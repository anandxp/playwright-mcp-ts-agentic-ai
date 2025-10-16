# 🤖 Agentic AI Testing Framework - Guide for Manual Testers

## Welcome! 👋

This framework lets you create **automated tests without writing any code**. You write test cases in plain English in Excel or CSV, and AI executes them automatically!

---

## 📝 How to Write Test Cases

### 1. Open the Test Case File

Open `test-cases/parking-tests.xlsx.csv` in Excel or any spreadsheet editor.

### 2. Fill in the Columns

| Column | What to Write | Example |
|--------|---------------|---------|
| **Test ID** | Unique identifier | TC001, TC002, TC003 |
| **Test Name** | Descriptive name | "Search parking in New York" |
| **Priority** | High, Medium, or Low | High |
| **Test Steps** | Steps in plain English (one per line) | Navigate to website<br>Enter address<br>Click search |
| **Expected Results** | What should happen (one per line) | Results should be displayed<br>Prices should be visible |
| **Status** | Active or Inactive | Active |

### 3. Writing Test Steps (Natural Language)

You can write steps naturally, as if you're explaining to a person:

#### Navigation
```
Navigate to https://demo.parkingbase.com/c/vignesh
Open the parking search page
Go to the homepage
```

#### Entering Text
```
Enter address '123 Main Street'
Search for parking at 'Times Square'
Type 'New York' in the location field
```

#### Clicking
```
Click search button
Click on the first garage
Click Reserve
Press the Filter button
```

#### Setting Dates/Times
```
Set Enter After as 'tomorrow 8:00 PM'
Set Exit Before as 'tomorrow 11:00 PM'
Change entry time to 'next Monday 9:00 AM'
```

#### Waiting
```
Wait for results to load
Wait 3 seconds
Wait for page to load
```

### 4. Writing Expected Results

Write what you expect to see:

```
Search results should be displayed
At least 5 parking options should be shown
URL should contain latitude and longitude
Prices should be visible for each option
Error message should appear
```

---

## 🚀 Running Tests

### Run ALL Active Tests
```bash
npm run test:ai
```

### Run Only HIGH Priority Tests
```bash
npm run test:ai:high
```

### Run Only MEDIUM Priority Tests
```bash
npm run test:ai:medium
```

### Run Only LOW Priority Tests
```bash
npm run test:ai:low
```

---

## 📊 Understanding Test Results

After tests run, you'll get:

### 1. Console Output
- Real-time progress of each test
- ✅ = Passed
- ❌ = Failed
- Step-by-step execution log

### 2. HTML Report (`test-report.html`)
- Beautiful visual report
- Summary with pass/fail counts
- Detailed logs for each test
- Screenshots of each step
- Error messages for failed tests

**To view report:** Double-click `test-report.html` in Windows Explorer

### 3. Screenshots Folder
- Screenshot after each step
- Failure screenshots when tests fail
- Located in `screenshots/` folder

---

## 💡 Tips for Writing Good Test Cases

### ✅ DO:
- Write clear, specific steps
- Use actual addresses and data
- One action per step
- Include verification steps
- Use Active status for tests to run

### ❌ DON'T:
- Make steps too complex
- Skip verification steps
- Leave expected results vague
- Forget to set priority

---

## 📝 Example: Complete Test Case

```csv
Test ID: TC011
Test Name: Book parking for weekend
Priority: High

Test Steps:
Navigate to https://demo.parkingbase.com/c/vignesh
Enter address 'Empire State Building, New York'
Set Enter After as 'next Saturday 10:00 AM'
Set Exit Before as 'next Saturday 8:00 PM'
Click search button
Wait for results to load
Click on first garage with rating above 4 stars
Click Reserve button

Expected Results:
Search results should be displayed
At least 3 parking options should be shown
Garage details should open
Reserve button should be clickable
Confirmation page should load
```

---

## 🔧 Troubleshooting

### Test Failed? Check:
1. Is the website URL correct?
2. Are the steps clear and specific?
3. Does the expected result match what actually happens?
4. Look at the screenshot in `screenshots/` folder
5. Read the error message in the HTML report

### Need Help?
1. Check existing test cases for examples
2. Review the failure screenshot
3. Ask your team lead
4. Update the test case and try again

---

## 🎯 Test Case Templates

### Template 1: Search Flow
```
Test Steps:
Navigate to [URL]
Enter address '[ADDRESS]'
Set dates and times
Click search
Verify results

Expected Results:
Results should be displayed
Data should be correct
```

### Template 2: Filter Test
```
Test Steps:
Perform a search
Click Filter button
Select filter option '[OPTION]'
Apply filter

Expected Results:
Filtered results should show
Filter should remain selected
```

### Template 3: Navigation Test
```
Test Steps:
Navigate to [PAGE]
Click on [ELEMENT]
Verify page loads

Expected Results:
Correct page should open
Content should be visible
```

---

## 📈 Scaling to 100+ Tests

### Organization Strategy:

1. **Group by Feature**
   - TC001-TC020: Search functionality
   - TC021-TC040: Booking flow
   - TC041-TC060: User account
   - TC061-TC080: Payment
   - TC081-TC100: Admin features

2. **Use Priorities**
   - **High**: Critical business flows (run daily)
   - **Medium**: Important features (run weekly)
   - **Low**: Edge cases (run monthly)

3. **Maintain Regularly**
   - Mark obsolete tests as "Inactive"
   - Update test steps when UI changes
   - Add new tests for new features

---

## 🎉 Benefits

### For Manual Testers:
- ✅ No coding required
- ✅ Write tests like documentation
- ✅ Immediate feedback
- ✅ Professional test reports
- ✅ Learn automation concepts

### For Team:
- ✅ Faster testing cycles
- ✅ Consistent test execution
- ✅ Better test coverage
- ✅ Easy to maintain
- ✅ Scales to 100+ tests

---

## 🆘 Quick Reference

### Common Actions
| Action | How to Write |
|--------|--------------|
| Click | `Click [element]` |
| Type | `Enter '[text]'` |
| Navigate | `Navigate to [url]` |
| Wait | `Wait for [thing]` |
| Verify | In Expected Results column |
| Select | `Select [option]` |
| Check | `Check [checkbox]` |

### Common Verifications
| Verification | How to Write |
|--------------|--------------|
| Visible | `[Thing] should be displayed` |
| Count | `At least X items should be shown` |
| URL | `URL should contain [text]` |
| Text | `[Text] should appear` |
| Error | `Error message should show` |

---

## 📞 Support

If you have questions:
1. Check this guide first
2. Look at example test cases
3. Review the HTML report for failures
4. Ask your team lead
5. Document new patterns you discover!

---

**Happy Testing! 🚀**

*Remember: You're not just a manual tester anymore - you're an AI-powered automation engineer!*

