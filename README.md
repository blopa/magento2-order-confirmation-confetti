# Werules_ConfirmationConfetti

**Werules/ConfirmationConfetti** is a Magento 2 module that adds a custom confetti effect and message to the order confirmation page. This module is designed to enhance the customer experience by celebrating their purchase in a fun and interactive way.

## Features
- Displays a custom thank-you message on the order confirmation page.
- Triggers a confetti animation effect for a celebratory touch.
- Fully configurable and easy to integrate into any Magento 2 store.

## Installation

1. Clone or download this repository into your Magento 2 `app/code` directory:
   ```bash
   cd app/code
   git clone https://github.com/yourusername/Werules_ConfirmationConfetti.git Werules/ConfirmationConfetti
   ```

2. Enable the module:
   ```bash
   php bin/magento module:enable Werules_ConfirmationConfetti
   php bin/magento setup:upgrade
   php bin/magento cache:flush
   ```

3. Deploy static content:
   ```bash
   php bin/magento setup:static-content:deploy -f
   ```

## Usage

Once installed and configured, the module will automatically add the following to the order confirmation page:

- A custom thank-you message.
- A confetti animation effect triggered after the page loads.

## Customization

### JavaScript Customization
The confetti animation is handled by a `confetti.js` file. You can find it at:
```
app/code/Werules/ConfirmationConfetti/view/frontend/web/js/confetti.js
```
You can customize this file to modify the confetti effect according to your store’s branding or preferences.

### Thank-You Message
The thank-you message is rendered in a `.phtml` template:
```
app/code/Werules/ConfirmationConfetti/view/frontend/templates/confetti.phtml
```
Update this file to change the text or HTML structure of the message.

### Layout Customization
The module uses the `checkout_onepage_success.xml` layout file to add the block and JavaScript to the order confirmation page:
```
app/code/Werules/ConfirmationConfetti/view/frontend/layout/checkout_onepage_success.xml
```
Edit this file if you need to change the placement of the message or script.

## Troubleshooting

1. **Confetti Effect Not Showing:**
    - Verify that `confetti.js` is loaded in the browser console.
    - Ensure that static content has been deployed and caches are cleared.

2. **Error in Console:**
    - Check for errors in your browser console to debug any JavaScript issues.
    - Ensure that `confetti.js` is properly loaded from the `pub/static` directory.

3. **Custom Message Not Appearing:**
    - Confirm that the module is enabled using:
      ```bash
      php bin/magento module:status
      ```
    - Verify that the layout and `.phtml` files are correctly placed and configured.

## Contributing
Contributions are welcome! If you’d like to improve this module, feel free to fork the repository and submit a pull request.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Support
For any issues or questions, please open an issue on this repository or contact the maintainer.
