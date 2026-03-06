# GitHub SAML Auto-Continue

A minimal Chrome extension that automatically clicks the "Continue" button on GitHub's SAML SSO page for the **oslokommune** organization.

No more manually clicking through the "Single sign-on to Oslo kommune" screen every time.

## Getting the source

**Option A: Clone with git**

```bash
git clone https://github.com/oslokommune/auto-saml-clicker.git
```

**Option B: Download as ZIP**

1. Go to the [repository page](https://github.com/oslokommune/auto-saml-clicker)
2. Click the green **Code** button
3. Select **Download ZIP**
4. Extract the ZIP to a folder on your machine

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
