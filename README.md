# Dental Case Board

A single-file checklist app for tracking veterinary dental cases from exam through next-day review.

**Live app:** https://jjdiaz9.github.io/dental-case-board/

- Works offline in the browser; cases are saved in the browser's local storage.
- This repository holds **only the app code** — no patient data.
- Optional sync stores the case file in a separate **private** repository through the GitHub Contents API, using a fine-grained token kept only in the browser.
- The checklist is editable in the app (**Edit checklist**).
- Can be installed on an iPad or iPhone: open the live app in Safari, tap **Share → Add to Home Screen**.
- Written prescriptions print from a case (letter size: original + records copy). The clinic logo and Rx symbol live in `rx/`; the prescriber's name and license number are entered in the app, not stored here.
- On a computer (Chrome or Edge), the app can be connected to the OneDrive records folder to confirm each visit's surgery report (Word file with the procedure date in its name) and scanned record (PDF) are there. Only folder/file names and dates are looked at, locally in the browser.
- Optional: with a Claude API key saved on the computer, "Controlled substances checked" can read the visit's scanned record with Claude and list the Colorado controlled substances given and dispensed, plus any gabapentin, as written. "Read all cases for this day" reads each of that day's records in turn, one request per record. A PDF is sent to the Claude API only when a button is pressed.
- Previous visit protocol: on a computer, "Find previous visits" (under "Anesthesia protocol written & handed off") lists the scanned records in the pet's records folder dated before this visit. "Read protocol" reads the one picked with Claude (same API key as the controlled substances reader) and saves the drug protocol, as written, on the case. "Copy protocol" copies it as text, and the filled-in drug sheet gets it on a "Previous protocol" tab.
