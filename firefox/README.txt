Firefox Extension Installation Instructions
=====================================

Due to Firefox's signing requirements, there are several ways to use these extensions:

Option 1: Temporary Installation (Easiest, but only lasts until Firefox restarts)
----------------------------------------------------------------
1. Open Firefox and go to about:debugging
2. Click 'This Firefox'
3. Click 'Load Temporary Add-on...'
4. Browse to the folder for each extension and select the manifest.json file

Option 2: Use Firefox Developer Edition or Nightly
----------------------------------------------------------------
1. Download and install Firefox Developer Edition or Firefox Nightly
2. Go to about:config and set xpinstall.signatures.required to false
3. Then you can install the .xpi files directly

Option 3: Use Firefox ESR
----------------------------------------------------------------
1. Download and install Firefox ESR
2. Go to about:config and set xpinstall.signatures.required to false
3. Then you can install the .xpi files directly

Option 4: Submit to Mozilla for Official Signing
----------------------------------------------------------------
For permanent installation in regular Firefox:
1. Create a developer account at https://addons.mozilla.org
2. Use web-ext tool to package and submit your extension:
   npm install -g web-ext
   cd [extension_folder]
   web-ext lint
   web-ext build
3. Upload the generated .zip file to https://addons.mozilla.org/developers/
4. Wait for Mozilla review and approval
