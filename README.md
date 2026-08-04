# 🚗 Vehicle Listing Form - "Sell Your Car"

A modern, accessible, and fully validated web form developed in **HTML5** and stylized in **CSS** for creating car sales listings. This project demonstrates best practices in HTML form structure, proper input-label binding, native field validations (`required`), accessibility considerations, and multi-file uploading.

---

## 📌 About the Project

This page provides a clean and intuitive user interface allowing sellers to post an advertisement for their vehicle. Users can enter essential car details such as title, price, brand, model, description, purchase date, transmission type, optional features, and upload photos.

---

## 🛠️ Educational Code Breakdown

Here is a step-by-step explanation of how the HTML code is structured:

### 1. Document Metadata & Setup (`<head>`)
Contains configurations required for browsers to process and render the page properly:

* `<!DOCTYPE html>`: Declares that the document complies with the **HTML5** standard.
* `<html lang="en">`: Specifies the primary language of the document.
* `<meta charset="UTF-8">`: Enables character encoding support for special characters and accents.
* `<meta name="viewport" content="...">`: Ensures responsive web design, fitting mobile phones, tablets, and desktops.
* `<link rel="stylesheet" href="css-form/style.css">`: Connects the external CSS stylesheet to style the form visually.
* `<title>`: Sets the text shown on the browser tab (*"Venda seu carro"*).

---

### 2. Main Layout Structure (`<body>`)

* `<p class="outphrase">`: A call-to-action phrase styled outside the main card container to attract user attention.
* `<div class="divmom">`: The main wrapper (parent container) grouping all form components for layout control and CSS centering.
* `<h1>` and `<h2>`: Section headings establishing visual and semantic hierarchy.

---

### 3. Interactive Form Components (`<form>`)

All user inputs are wrapped inside the `<form>` element:

#### 🔹 Mandatory Fields & Text Inputs (`<input>` & `<textarea>`)
* **Required Fields (`required`)**: Essential fields such as Title, Price, Description, Brand, Model, Mileage, Date, Transmission, and Photos include the `required` attribute. This triggers native browser validation, preventing form submission if any mandatory field is empty.
* **Ad Title**: Uses `minlength="1"` and `maxlength="30"` to enforce input boundaries.
* **Price**: Uses `type="number"` to ensure numerical input and open mobile number keypads automatically.
* **Description**: Employs a `<textarea>` tag to support multi-line text for vehicle condition notes and extra details.
* **Asterisks (`<span class="asterisk">*</span>`)**: Visual indicators communicating required fields to users.

#### 🔹 Date Picker (`<input type="date">`)
* Renders a native date picker calendar for selecting the vehicle's **Purchase Date**.

#### 🔹 Single-Choice Selection / Radio Buttons (`<input type="radio">`)
* Used for **Transmission Type** (*Manual* or *Automatic*).
* Both `<input>` elements share the exact same `name="gear"`, ensuring mutual exclusion (only one option can be selected at a time).

#### 🔹 Multiple-Choice Checkboxes (`<input type="checkbox">`)
* Organized cleanly within unordered lists (`<ul>` and `<li>`).
* Allows users to select multiple **Optional Features** (e.g., *Airbag*, *Air Conditioning*, *Rear Camera*, *Keyless Entry*, *Leather Seats*).
* `name="optionals[]"`: Uses array notation so backend scripts can process all selected checkboxes as a list.

#### 🔹 File Upload (`<input type="file">`)
* Used for attaching **Car Photos**.
* `multiple`: Permits uploading several images at once.
* `accept="image/png, image/jpg"`: Restricts valid selections exclusively to PNG and JPG image files.

#### 🔹 Form Submission (`<input type="submit">`)
* Renders the **CADASTRAR** button that sends the collected data when pressed.

---

## ♿ Accessibility & Best Practices Highlighted

1. **Explicit Label Binding (`for` + `id`):** Every field links `<label for="x">` to `<input id="x">`. Clicking on a label's text automatically focuses or toggles its corresponding input, which greatly assists screen reader users and touchscreens.
2. **Native Form Validation:** Using native HTML5 validation attributes (`required`, `type="number"`, `minlength`/`maxlength`) provides instant feedback to users without needing external JavaScript libraries.
3. **Array Data Structure:** Using `name="optionals[]"` for checkboxes ensures backend readiness for array-based data handling (e.g., in PHP or Node.js).
