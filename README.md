# GitHub SAML Auto-Continue

A minimal Chrome extension that automatically clicks the "Continue" button on GitHub's SAML SSO page for the **oslokommune** organization.

No more manually clicking through the "Single sign-on to Oslo kommune" screen every time.

## Installation

1. Open Chrome and navigate to `chrome://extensions/`
2. Enable **Developer mode** using the toggle in the top-right corner
3. Click **Load unpacked**
4. Select the `auto-saml-clicker` folder

## How it works

The extension runs a content script on GitHub pages that looks for the SAML initiation form for `oslokommune`. When found, it automatically submits the form — effectively clicking "Continue" for you.

If the page loads dynamically, it watches for DOM changes and clicks the button as soon as it appears (with a 10-second timeout).

## Updating

After making changes to the extension files, go to `chrome://extensions/` and click the refresh icon on the extension card.
