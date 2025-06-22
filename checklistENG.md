# ✅ Checklist for Form Testing (Test Task)

**Description:**  
This checklist was created as part of a test task for a QA position.  
The goal is to test the first screen of the insurance form. All checks are structured, prioritized, and accompanied by expected results.

## 1. Visual Interface (Priority - High)
- The banner is displayed correctly, without distortion.  
**Expected result:** The banner loads fully, without cropping, blurring, or distortion at all resolutions.
- The page title is displayed correctly.  
**Expected result:** The text "Mortgage Insurance" is readable, does not overflow, and is styled properly.
- The "Property / Life / Property+Life" toggles are displayed and function correctly.  
**Expected result:** The active tab is visible, others are clickable, switching updates the interface.
- The button is present and visually stands out.  
**Expected result:** The button is noticeable, has a contrasting color, and stands out from the background.
- All form elements are aligned and do not overlap.  
**Expected result:** Fields and labels are neatly arranged, with no visual shifts or overlaps.
- Fonts, colors, and spacing match the site's overall style.  
**Expected result:** Unified fonts, sizes, and spacing are used across the screen.
- Animations play smoothly.  
**Expected result:** No lags or stutters when lists open.
- All elements load evenly.  
**Expected result:** All blocks appear in sync.
- The cursor changes to pointer when hovering over clickable elements.  
**Expected result:** On hover, the cursor changes to pointer for buttons/links.

## 2. Input Fields (Priority - High)
### 2.1 General Field Checks
- Check inserting values from clipboard.  
**Expected result:** Only valid values can be pasted.
- Field is cleared after input.  
**Expected result:** The field is empty after clearing.
- Leading and trailing spaces are trimmed.  
**Expected result:** Extra spaces are automatically removed when filling out the form.
- Field is required.  
**Expected result:** Form cannot be submitted without a value, field is highlighted.

### 2.2 Bank That Issued the Mortgage
- Dropdown opens and displays options.  
**Expected result:** List is displayed correctly, all values are readable.
- Value can be selected via mouse and keyboard.  
**Expected result:** Selection via click or keys.
- Search works by first letters.  
**Expected result:** Relevant options appear when the first letter is typed.
- Submitting an empty field shows an error.  
**Expected result:** Form is not submitted, field is highlighted, error message is displayed.

### 2.3 Remaining Debt
- Only digits can be entered.  
**Expected result:** Letters and symbols cannot be entered or are deleted.
- Limits: minimum - 20000, maximum - 350000000.  
**Expected result:** Values outside the allowed range trigger an error.
- Error on invalid range.  
**Expected result:** Error message is displayed, field is highlighted.
- Letters and special characters cannot be entered.  
**Expected result:** Invalid characters do not appear or are cleared.
- Empty value triggers an error.  
**Expected result:** Form submission shows an error.

### 2.4 Your Gender
- Dropdown shows "Male" / "Female" options.  
**Expected result:** Both values available, list opens correctly.
- Selection via mouse and keyboard.  
**Expected result:** Selection via click or keys.
- Value should not change manually in console.  
**Expected result:** Values cannot be manipulated via DevTools.

### 2.5 Date of Birth
- Input via calendar and manual entry.  
**Expected result:** Works both ways.
- Limits: minimum age 18, maximum 75.  
**Expected result:** Out-of-range dates trigger an error.
- Error on invalid age.  
**Expected result:** Error message is shown, field is highlighted.
- Cannot enter letters or symbols.  
**Expected result:** Invalid characters are blocked or removed.
- Invalid format cannot be entered.  
**Expected result:** Formats like "abc", "1234-99-99" are blocked.

### 2.6 Property Type
- Dropdown opens and displays options.  
**Expected result:** List is displayed correctly, all values are readable.
- Value can be selected via mouse and keyboard.  
**Expected result:** Selection via click or keys.

### 2.7 Year Built
- Only digits can be entered.  
**Expected result:** Letters and symbols cannot be entered or are deleted.
- Limits: minimum - 1850, maximum - 2060.  
**Expected result:** Out-of-range values trigger an error.
- Error on invalid range.  
**Expected result:** Error message is displayed, field is highlighted.
- Letters and special characters are not allowed.  
**Expected result:** Invalid characters are blocked or removed.

### 2.8 Property Region
- Dropdown opens and displays options.  
**Expected result:** List is displayed correctly, all values are readable.
- Value can be selected via mouse and keyboard.  
**Expected result:** Selection via click or keys.
- Search works by first letters.  
**Expected result:** Relevant options appear when the first letter is typed.

### 2.9 DevTools Check
- In Elements tab - check required HTML attributes.  
**Expected result:** All fields contain necessary HTML attributes.
- In Console tab - no errors.  
**Expected result:** No errors appear.
- In Network tab - form sends POST request.  
**Expected result:** POST request includes correct data.
- Request body values match input values.  
**Expected result:** Submitted data matches entered values.
- Server responds correctly.  
**Expected result:** Valid HTTP response code from server.

## 3. Checkboxes (Priority - Medium)
- Clickable.  
**Expected result:** Clicking changes state.
- Actual state is shown.  
**Expected result:** Checked state shows a tick; unchecked shows nothing.
- State persists after clicking.  
**Expected result:** Value is reflected in the request and UI.
- No interference between checkboxes.  
**Expected result:** Changing one checkbox does not affect others.
- Network tab shows checkbox values.  
**Expected result:** Value sent as true/false or 1/0 in request body.

## 4. Validation and Errors (Priority - High)
- Real-time validation.  
**Expected result:** Leaving field with error shows highlight and message.
- Clear, visible error messages.  
**Expected result:** Message is shown near field and easy to understand.
- Error text is red.  
**Expected result:** Follows standard expectation.
- Error disappears after fix.  
**Expected result:** Highlight and error message are removed.
- Cannot submit form with invalid/empty fields.  
**Expected result:** Submit button is active, but no request sent, errors are shown.
- Retesting without changes keeps errors.  
**Expected result:** Form is not submitted, errors remain.
- No Console (DevTools) errors.  
**Expected result:** No errors during input/validation.

## 5. “See Offers” Button (Priority - High)
- Changes style and cursor on hover.  
**Expected result:** Cursor becomes pointer, color changes.
- No request sent with invalid/empty fields; shows errors.  
**Expected result:** No request in Network tab, field errors appear.
- Sends valid POST request.  
**Expected result:** POST with correct fields, 200 OK.
- No duplicate request on repeat click.  
**Expected result:** No duplicate calls in Network tab.

## 6. Security (Priority - High)
- HTTPS protocol.  
**Expected result:** Page loads via https://, no browser warnings.
- Test XSS and SQL injection.  
**Expected result:** Input is shown as text, not executed.
- Scripts in fields should not execute.

## 7. Responsiveness (Priority - Medium)
- Proper display at various resolutions (1920x1080, 1440x900, 1024x768, 768x1024, 374x667).  
**Expected result:** All elements visible, no overlapping.
- Cross-browser compatibility.  
**Expected result:** Elements display and work the same in all major browsers.
- No horizontal scroll.  
**Expected result:** Page doesn't scroll sideways.
- Buttons and form elements remain clickable.  
**Expected result:** Elements stay within screen bounds and accessible.
- Screen rotation on phone.  
**Expected result:** Layout adapts correctly.

## 8. Accessibility (Priority - Low)
- Tab navigation.  
**Expected result:** Can navigate all fields and buttons with keyboard.
- Focus on active elements.  
**Expected result:** Active field is highlighted, focus is visible.
- Screen reader check.  
**Expected result:** Fields and buttons are read out properly.

## 9. Postman (Priority - High)
- Test API with manual POST.  
**Expected result:** Server returns 2xx OK for valid data, 4xx for errors.
- Server-side validation.  
**Expected result:** Invalid data triggers error from server.
- Required fields check.  
**Expected result:** Server shows validation error for missing required fields.
- Boundary and string length tests.  
**Expected result:** Exceeding limits triggers error.
- Check headers and authorization.  
**Expected result:** Server handles tokens correctly.

## 10. Performance (Priority - Medium)
- First screen load time (DevTools Performance).  
**Expected result:** FCP is less than 2 seconds.