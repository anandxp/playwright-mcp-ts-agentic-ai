# 🚀 Quick Start in 5 Minutes

## For Manual Testers - NO CODING REQUIRED!

### Step 1: Open Test Case File (1 minute)

Open `test-cases/parking-tests.xlsx.csv` in **Excel** or **Notepad**

### Step 2: Write Your Test (2 minutes)

Copy this example and modify it:

```csv
TC001,Search for parking,High,"Navigate to https://demo.parkingbase.com/c/vignesh
Enter address 'Times Square New York'
Click search button","Results should be displayed
Prices should be visible",Active
```

**That's it!** You just wrote an automated test in plain English!

### Step 3: Run Your Tests (1 minute)

Open **Command Prompt** or **PowerShell** in this folder and type:

```bash
npm run test:ai
```

Press Enter and watch AI execute your test!

### Step 4: View Results (1 minute)

Double-click `test-report.html` to see:
- ✅ Which tests passed
- ❌ Which tests failed  
- 📸 Screenshots of every step
- 📊 Beautiful visual report

---

## 🎯 What You Can Test (Examples)

### Search Tests
```
Navigate to [URL]
Enter address 'New York'
Click search
```

### Booking Tests
```
Search for parking
Click on first result
Click Reserve button
```

### Filter Tests
```
Search for parking
Click Filter
Select 'Under $50'
Apply filter
```

---

## 📝 Writing Test Steps (Natural Language)

| What You Want | How to Write It |
|---------------|-----------------|
| Go to website | `Navigate to https://...` |
| Type something | `Enter address 'text here'` |
| Click button | `Click search button` |
| Wait | `Wait for results to load` |
| Select date | `Set Enter After as 'tomorrow 8:00 PM'` |

---

## 🎓 Learning Path

### Day 1: Run existing tests
```bash
npm run test:ai
```

### Day 2: Modify one test
Change an address or step

### Day 3: Create your first test
Copy TC001 and modify it

### Week 1: Create 5-10 tests
Cover different features

### Month 1: Master the framework
Create 50+ tests

### Month 2+: Scale to 100+ tests
Become an automation expert!

---

## 🆘 Need Help?

1. **Read**: `MANUAL_TESTER_GUIDE.md` (detailed guide)
2. **Examples**: Look at existing tests in CSV file
3. **Reports**: Check `test-report.html` for errors
4. **Screenshots**: Look in `screenshots/` folder

---

## 🎉 Congratulations!

You're now an **AI-Powered Automation Engineer**! 

No coding required - just write in English and let AI do the work! 🚀

---

## 📞 Common Commands

```bash
# Run ALL tests
npm run test:ai

# Run only HIGH priority tests (critical tests)
npm run test:ai:high

# Run only MEDIUM priority tests
npm run test:ai:medium

# Run only LOW priority tests
npm run test:ai:low
```

---

**Next Steps:**
1. Read `MANUAL_TESTER_GUIDE.md` for complete documentation
2. Try running the example tests
3. Create your first test
4. Share with your team!

**Remember:** If you can write an email, you can write automated tests! ✨

