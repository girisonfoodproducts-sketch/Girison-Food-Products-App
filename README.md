# Girison Food Products Android App

Native Android Java app for Girison Food Products / Assam Royal Tea. It fetches products and selling prices from `https://www.girisonfoodproducts.online/api/products.php`, provides Leaf/Dust filters, cart quantity controls, and prepares an order message to hand off to WhatsApp.

## Build with GitHub Actions
1. Extract this ZIP.
2. Create a **new** GitHub repository.
3. Upload all extracted project files and folders, including `.github/workflows/android-apk.yml`. Do not upload the outer folder itself; upload its contents.
4. Open **Actions** → **Build Girison Food Products APK** → **Run workflow**.
5. When the run succeeds, download the `GirisonFoodProducts-debug-apk` artifact and extract `app-debug.apk`.

The workflow avoids `android-actions/setup-android`, which previously failed while looking for the legacy `tools` package. It locates the SDK manager already installed on the GitHub runner and installs the required packages directly. This workflow still needs to be run on GitHub to verify the build.

## Note
This is a debug APK for testing, not a Play Store-signed release. WhatsApp checkout prepares a message for the customer to review and send; it does not save the order into the website database.
