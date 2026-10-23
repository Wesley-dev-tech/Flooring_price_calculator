# Vloermeester bv — Flooring Price Calculator

A course project during my developer training: a website for a fictional tiling company, with a price calculator for private customers and a downloadable pdf.

## The Assignment

Build an application for a floor tiler (someone who lays tiles in your home):

- Add customer contact details and the room dimensions.
- Choose a tile type, joint type and joint colour.
- Do the calculation.
- Show the price in an alert and create a quote.
- Use `Number()` to convert the input.
- Round prices to two decimal places.

The layout was free to choose, but had to use Bootstrap, Bootstrap Grid, Flexbox, Google Fonts, Font Awesome icons, responsive design and a colour palette from Coolors.co. No other frameworks were allowed.

## Technologies Used

- HTML for the page content and the price form.
- CSS for the house style, using a Coolors.co colour palette stored as CSS variables.
- JavaScript for reading the form, calculating the price and filling in the quote.
- Bootstrap 5.3.3 for the responsive grid, cards, tables and the collapsible navigation.
- jsPDF for generating downloadable A4 quote PDFs in the browser.
- Flexbox for aligning content inside the grid columns.
- Google Fonts: Montserrat for headings and Plus Jakarta Sans for body text.
- Font Awesome 6.5.2 for the icons.

## Features

- A responsive one-page website with a hero, services, price calculator and contact section.
- A price form with name, length, width, joint thickness and joint colour.
- Input validation with an alert when a field is missing or invalid.
- Price calculation and 21% VAT. Customers can also choose to supply their own tiles.
- An alert with the price excluding and including VAT, rounded to two decimals.
- A branded quote with customer contact details, project details, a price breakdown, a unique quote number and a 30-day validity period. Numbers use Belgian formatting (for example, `1.234,56`).
- A "Download als PDF" button that generates and downloads an A4 PDF quote using jsPDF.
- A footer with the company's (fictional) contact details: e-mail, phone, registered office and company number, spread over three columns. The on-screen quote and the PDF use the same footer layout, with the company address under "Van".
- Cache busting: `style.css` and `app.js` are loaded with a version number (`?v=1.4.0`), so browsers load the latest version after an update.
- A mobile menu that closes automatically after choosing a section.

## What I Practised

Selecting elements with `getElementById`, handling click events, reading and converting form input, writing calculations with `if`/`else` validation, using template literals, formatting numbers with `Intl.NumberFormat`, updating the page with `textContent`, and generating a PDF quote.

## How to View

Download the files and open `index.html` in a browser. No installation or build step is required. An internet connection is needed to load Bootstrap, jsPDF, Google Fonts and Font Awesome.

To download a quote as PDF: complete the form, calculate a price and click **Download als PDF**. On iPhone, Safari may open the PDF or offer its download/share controls; use the share menu's **Save to Files** option to keep a copy.

## Project Structure

- `index.html`: the page structure and the quote template.
- `style.css`: the house style and layout details.
- `app.js`: the price calculation, quote and mobile menu.
- `README.md`: project documentation.

## About This Version

Current version: **1.4.0**. After changing `style.css` or `app.js`, raise the `?v=` number on both links in `index.html` so visitors don't get an old cached copy.

Vloermeester bv is a fictional company created for a school assignment, and the rates are fictional. The contact details are deliberately invalid so they can't belong to a real company: the e-mail address uses the reserved `.example` domain, the phone number `+32 (0)14 01 23 45` can't exist (Belgian subscriber numbers never start with 0), and the company number `BE 0123.456.789` fails the official modulo-97 check. The quote is an indication only; additional materials, preparation work and extra costs are not included. This is a static frontend demo: form data is processed in the browser and nothing is sent to or stored by a server.
