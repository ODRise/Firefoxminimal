# Firefox Custom CSS

This repository contains a `userChrome.css` file to customize the appearance of the Firefox browser. The CSS aims to provide a cleaner, more minimalist look by modifying various UI elements.

## Features

* **Square Tabs:** Removes the default rounded corners from tabs.

* **Consistent Tab Color:** Makes the active tab background color the same as non-active tabs for a uniform look.

* **Transparent Toolbars:** Makes the main toolbars (`navigator-toolbox`, `PersonalToolbar`, `nav-bar`) and the sidebar transparent.

* **Hidden UI Elements:** Hides window control buttons (Min/Max/Close), various urlbar icons, and the back/forward buttons.

* **Custom Fonts:** Sets custom fonts for the urlbar and the application menu.

* **Tab Customization:** Centers tab icons and labels, and adjusts the opacity and hover behavior of the tab close button.

* **Speaker Icon Styling:** Customizes the appearance of the tab speaker icon.

* **Urlbar Transparency:** Adds transparency to the urlbar background.

* **Removes Content Outline:** Removes the outline/box-shadow around the main content window.

## Installation

To use this custom CSS, you need to enable user stylesheets in Firefox and place the `userChrome.css` file in the correct directory.

1. **Enable User Stylesheets:**

   * Open a new tab in Firefox and type `about:config` in the address bar.

   * Accept the risk if prompted.

   * Search for `toolkit.legacyUserProfileCustomizations.stylesheets` and set the value to `true` by clicking the toggle button.

2. **Locate Your Firefox Profile Folder:**

   * Open a new tab and type `about:profiles` in the address bar.

   * Find the profile that is currently in use (it will say "This is the profile in use and it cannot be deleted.").

   * Click the "Open Folder" or "Open Directory" button next to "Root Directory". This will open your profile folder.

3. **Create `chrome` Folder and `userChrome.css` File:**

   * Inside your profile folder, create a new folder named `chrome` if it doesn't already exist. Note the lowercase 'c'.

   * Navigate into the newly created `chrome` folder.

   * Create a new text file named `userChrome.css` inside the `chrome` folder. Note the lowercase 'u', 'c', and 'css'.

4. **Add the CSS Code:**

   * Copy the content from the `userChrome.css` file in this repository.

   * Paste the copied code into the `userChrome.css` file you created in your profile's `chrome` folder.

   * Save the `userChrome.css` file.

5. **Restart Firefox:**

   * Close and reopen Firefox for the changes to take effect.

## Screenshot

![Screenshot of Firefox with Custom CSS](/x7kne2h2Md.png)

## Recommended Add-ons

Here are some add-ons that complement this custom CSS by further enhancing the minimalist look and feel of Firefox:

[OS style Close Window Button](https://addons.mozilla.org/en-US/firefox/addon/os-style-close-window-button/) - OS styleToolbar button to close current window.

[OS style Minimze Window Button](https://addons.mozilla.org/en-US/firefox/addon/os-style-minimze-window-button/) - OS style Toolbar button to Minimze current window.

[OS style Maxmize Window Button](https://addons.mozilla.org/en-US/firefox/addon/os-style-maxmize-window-button/) - OS style Toolbar button to Maxminize current window.

[Betterfox](https://github.com/yokoffing/BetterFox)

## Optional Betterfox Code

<details>
  <summary>Click to expand/collapse optional Betterfox code</summary>

      user_pref("apz.overscroll.enabled", true); // DEFAULT NON-LINUX
      user_pref("general.smoothScroll", true); // DEFAULT
      user_pref("general.smoothScroll.msdPhysics.continuousMotionMaxDeltaMS", 12);
      user_pref("general.smoothScroll.msdPhysics.enabled", true);
      user_pref("general.smoothScroll.msdPhysics.motionBeginSpringConstant", 600);
      user_pref("general.smoothScroll.msdPhysics.regularSpringConstant", 650);
      user_pref("general.smoothScroll.msdPhysics.slowdownMinDeltaMS", 25);
      user_pref("general.smoothScroll.msdPhysics.slowdownMinDeltaRatio", "2");
      user_pref("general.smoothScroll.msdPhysics.slowdownSpringConstant", 250);
      user_pref("general.smoothScroll.currentVelocityWeighting", "1");
      user_pref("general.smoothScroll.stopDecelerationWeighting", "1");
      user_pref("mousewheel.default.delta_multiplier_y", 300); // 250-400; adjust this number to your liking
      user_pref("gfx.font_rendering.cleartype_params.gamma", 1750); 
      user_pref("gfx.font_rendering.cleartype_params.rendering_mode", 5);
      user_pref("gfx.font_rendering.cleartype_params.enhanced_contrast", 50)
      user_pref("gfx.font_rendering.cleartype_params.cleartype_level", 100);
      user_pref("gfx.font_rendering.directwrite.use_gdi_table_loading", false); 
      user_pref("gfx.webrender.quality.force-subpixel-aa-where-possible", true); 
      user_pref("media.mediasource.vp9.enabled", 0);
      user_pref("accessibility.force_disabled", 1);

## Compatibility

This CSS relies on the `toolkit.legacyUserProfileCustomizations.stylesheets` preference being enabled. Please be aware that this is a legacy feature and its availability or behavior may change in future Firefox updates.
