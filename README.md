# qr
 
# QR Code Generator

A simple QR Code generator built using HTML, CSS, and JavaScript. This project allows users to input text or a URL, and generates a QR code with optional customization options.

## Features

- Generate QR codes from user input (text or URL)
- Optional logo integration
- Customizable colors for dots and background

## Demo

You can see a live demo of the project [here](#).

## Getting Started

### Prerequisites

No installation is needed. Just open the HTML file in a web browser.

### Usage

1. Clone or download the repository.
2. Open `index.html` in your preferred web browser.
3. Enter a URL or text in the input field.
4. Click the "Generate" button to create the QR code.
5. The generated QR code will appear below the button.

### Code Explanation

- The project uses the [QRCodeStyling](https://github.com/davidshimjs/qrcodejs) library for QR code generation.
- The QR code is generated as an SVG and can include a logo if desired.
- Styling is handled using CSS for a clean and responsive layout.

### Example Code

Here’s a snippet of the core functionality:

```html
<script>
    document.getElementById('generateBtn').onclick = function() {
        const qrInput = document.getElementById('qrInput').value;

        const qrCode = new QRCodeStyling({
            width: 300, height: 300, type: "svg",
            data: qrInput,
            image: "https://upload.wikimedia.org/wikipedia/commons/5/51/Facebook_f_logo_%282019%29.svg", // Optional logo
            dotsOptions: { color: "#4267b2", type: "rounded" },
            backgroundOptions: { color: "#e9ebee" },
            imageOptions: { crossOrigin: "anonymous", margin: 20 }
        });
        qrCode.append(document.getElementById("canvas"));
    };
</script>
