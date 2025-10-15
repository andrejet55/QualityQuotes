# Getting Started - Quick Guide

## 5-Minute Setup

### Step 1: Install Dependencies (1 minute)

```bash
# Make sure you're in the project directory
cd /home/user/QualityQuotes

# Install required packages
pip install pandas numpy matplotlib seaborn plotly faker scipy jupyter notebook
```

Or use the requirements file:

```bash
pip install -r requirements.txt
```

### Step 2: Launch Jupyter (30 seconds)

```bash
jupyter notebook
```

This will open your browser with the Jupyter interface.

### Step 3: Run the Notebooks (7 minutes)

In Jupyter, open and run each notebook **in order**:

#### Notebook 1: Generate Data (2 min)
1. Open `01_data_generation.ipynb`
2. Click "Cell" → "Run All"
3. Wait for completion (creates `data/` folder with CSV files)
4. You should see: "Data exported successfully!"

#### Notebook 2: Create Visualizations (3 min)
1. Open `02_visualizations.ipynb`
2. Click "Cell" → "Run All"
3. Scroll through to see 10 interactive charts
4. Hover over charts to see details

#### Notebook 3: Extract Insights (2 min)
1. Open `03_insights_report.ipynb`
2. Click "Cell" → "Run All"
3. Read through the 6 key insights
4. Copy recommendations for your report

### Step 4: Use the Results

Your data and visualizations are now ready to use in your report!

---

## What You'll Get

### After Notebook 1:
```
data/
├── users.csv          (5,000 user profiles)
├── quotes.csv         (40,000+ quote events)
├── interactions.csv   (60,000+ interactions)
└── sessions.csv       (25,000+ sessions)
```

### After Notebook 2:
- 10 interactive Plotly charts you can export
- Statistical summaries for each visualization
- Brand-colored, presentation-ready graphics

### After Notebook 3:
- 6 actionable insights with recommendations
- Quantified growth opportunities
- Strategic action plan (immediate/short/long-term)

---

## Export Charts for Your Report

### Option 1: Save as PNG (Static Image)

```python
# Add this to any cell in notebook 02
fig.write_image("category_performance.png", width=1200, height=600)
```

**Note**: Requires `kaleido` package:
```bash
pip install kaleido
```

### Option 2: Save as HTML (Interactive)

```python
# Add this to any cell in notebook 02
fig.write_html("category_performance.html")
```

Then open the HTML file in your browser and take screenshots.

### Option 3: Screenshot Directly

1. Run the visualization cell
2. Hover to remove any tooltips
3. Use your OS screenshot tool
4. Paste into your report

---

## Common Questions

### Q: Do I need to modify the code?

**A**: No! Just run the notebooks as-is. Everything is pre-configured with sensible defaults.

### Q: Can I change the number of users or time period?

**A**: Yes! In `01_data_generation.ipynb`, modify these variables:

```python
NUM_USERS = 5000  # Change to 10000 for more data
START_DATE = datetime(2025, 7, 1)  # Change dates as needed
END_DATE = datetime(2025, 9, 30)
```

Then re-run all three notebooks.

### Q: How do I export the entire notebook as PDF?

**A**: In Jupyter, go to File → Download as → PDF via LaTeX (requires LaTeX installation)

Or use command line:
```bash
jupyter nbconvert --to pdf 03_insights_report.ipynb
```

### Q: The charts aren't showing up!

**A**: Try these:
1. Restart the kernel: Kernel → Restart & Run All
2. Make sure Plotly is installed: `pip install plotly --upgrade`
3. Check browser console for errors (F12)

### Q: Can I run this without Jupyter?

**A**: Yes, but Jupyter is recommended. You could convert to Python scripts:
```bash
jupyter nbconvert --to script 01_data_generation.ipynb
python 01_data_generation.py
```

---

## Tips for Your Report

### 1. Methodology Section

Copy from `workflow_diagram.md`:
- "Data Generation Strategy" section
- "Statistical Distributions Used"
- "Technical Challenges & Solutions"

### 2. Results Section

Use visualizations from notebook 02:
- Export 4-5 key charts as images
- Include chart titles and captions
- Reference specific findings

### 3. Insights Section

Copy from notebook 03:
- Each of the 6 insights
- Supporting statistics
- Recommendations

### 4. Discussion Section

Use from `PROJECT_SUMMARY.md`:
- "Why This Stack?" rationale
- "What Makes This Implementation Strong"
- Technical design decisions

### 5. Conclusion

Use from notebook 03:
- Strategic recommendations summary
- Success metrics
- Next steps

---

## Troubleshooting

### Error: "ModuleNotFoundError: No module named 'plotly'"

**Fix**: Install missing package
```bash
pip install plotly
```

### Error: "FileNotFoundError: data/users.csv"

**Fix**: Run notebook 01 first to generate data files

### Error: "Kernel died"

**Fix**: You may have too many users. Reduce `NUM_USERS` to 2000 in notebook 01

### Charts show but no interactivity

**Fix**: Make sure you're viewing in Jupyter, not a static export

---

## Time Estimates

| Task | Time |
|------|------|
| Install dependencies | 1-2 min |
| Run notebook 01 (data generation) | 2 min |
| Run notebook 02 (visualizations) | 3 min |
| Run notebook 03 (insights) | 2 min |
| Export 5 charts for report | 5 min |
| **Total** | **13-15 min** |

---

## Next Steps After Setup

1. ✅ Read `PROJECT_SUMMARY.md` for overview
2. ✅ Review `README.md` for detailed documentation
3. ✅ Check `workflow_diagram.md` for technical details
4. ✅ Run all three notebooks
5. ✅ Export charts you need
6. ✅ Write your report using the insights!

---

## Quick Command Reference

```bash
# Install
pip install -r requirements.txt

# Launch Jupyter
jupyter notebook

# Export chart (in Python)
fig.write_image("chart.png")
fig.write_html("chart.html")

# Export notebook to PDF
jupyter nbconvert --to pdf notebook.ipynb

# Export notebook to HTML
jupyter nbconvert --to html notebook.ipynb
```

---

**You're ready to go! Start with notebook 01 and work your way through.** 🚀

Good luck with your case study! 📊✨
