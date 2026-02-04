# Phase 01: Core Rebranding - Version Info and Window Titles

This phase establishes the foundational rebranding from "Notepad++" to "Notepad+-" by updating the core version information, window titles, and main application resources. This creates the immediate user-facing brand identity visible in the window title, taskbar, and file properties.

## Tasks

- [x] Update version information and URLs in resource.h:
  - Review `/PowerEditor/src/resource.h` for current NOTEPAD_PLUS_VERSION, INFO_URL, and FORCED_DOWNLOAD_DOMAIN values
  - Update INFO_URL and FORCED_DOWNLOAD_DOMAIN to point to your GitHub repository
  - Ensure NOTEPAD_PLUS_VERSION reflects "Notepad+-" branding
  - Keep VERSION_MAJOR, VERSION_MINOR, VERSION_BUILD, and VERSION_VALUE appropriate for the fork

- [x] Update version resource block in Notepad_plus.rc:
  - Edit `/PowerEditor/src/Notepad_plus.rc` version info block (around lines 28-55)
  - Update CompanyName to your name/organization
  - Update LegalCopyright to reflect your fork (e.g., "Copyleft 1998-2023 by Don HO, Modified 2025 by [Your Name]")
  - Verify FileDescription, InternalName, OriginalFilename, and ProductName all say "Notepad+-"
  - Note: These may already be branded based on the discovery conversation - verify consistency

- [x] Update window class name in Notepad_plus_Window.h:
  - Verified line 69 of `/PowerEditor/src/Notepad_plus_Window.h` has window class name as "Notepad+-"
  - Confirmed consistency: the `_className` is properly used in `Notepad_plus_Window.cpp` at lines 78 and 101 for RegisterClass and CreateWindowEx calls

- [x] Update URLs in NppCommands.cpp:
  - Edit `/PowerEditor/src/NppCommands.cpp` line 3636 - replace `https://notepad-plus-plus.org/` with your GitHub URL
  - Edit line 3659 - replace forum URL or remove the forum menu item entirely
  - Edit line 3679 - replace downloads URL with your GitHub releases URL

- [ ] Update donation URL in Notepad_plus.cpp:
  - Edit `/PowerEditor/src/Notepad_plus.cpp` line 7789
  - Replace `https://notepad-plus-plus.org/donate/` with your GitHub sponsorship page or remove if not applicable

- [ ] Update About box home page URL:
  - Edit `/PowerEditor/src/WinControls/AboutDlg/AboutDlg.cpp` line 144
  - Replace `L"https://notepad-plus-plus.org/"` with your GitHub repository URL

- [ ] Update menu resource strings for Help menu:
  - Edit `/PowerEditor/src/Notepad_plus.rc` around lines 1343-1351
  - Update "Notepad+- Home" and "Notepad+- Project Page" URLs
  - Update "Notepad+- Online User Manual" URL if applicable
  - Update "Notepad+- Community (Forum)" or remove if not using a forum
  - Change "About Notepad++" to "About Notepad+-" (IDM_ABOUT)
