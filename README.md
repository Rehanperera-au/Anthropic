# Anthropic

# GitHub Codespaces Workflow for Python

Here's a simple workflow for testing and checking in code to your GitHub repository using Codespaces:

## Basic Git Commands

```bash
# Check status of your files
git status

# Add your changes to staging
git add filename.py  # For specific file
git add .            # For all changes

# Commit your changes
git commit -m "Brief description of your changes"

# Push to GitHub
git push origin main  # Replace 'main' with your branch name if different
```

## Simple Python Test Script

Create a file called `test_setup.py`:

```python
# Simple test script to verify your Python environment
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import os

# Print installed package versions
print(f"Python version: {pd.__version__}")
print(f"NumPy version: {np.__version__}")
print(f"Matplotlib version: {plt.__version__}")

# Create and manipulate a simple DataFrame
data = {'Name': ['Alice', 'Bob', 'Charlie'],
        'Age': [25, 30, 35],
        'Score': [85.5, 92.0, 78.5]}

df = pd.DataFrame(data)
print("\nTest DataFrame:")
print(df)

# Basic analysis
print("\nBasic Statistics:")
print(df.describe())

# Print current directory contents
print("\nFiles in current directory:")
print(os.listdir('.'))

print("\nSetup test completed successfully!")
```

## Testing and Committing Workflow

1. **Create and test your script**:
   ```bash
   # Create the test file
   touch test_setup.py
   # Paste the code above using the editor
   # Run the script
   python test_setup.py
   ```

2. **Check status and commit**:
   ```bash
   # See what files were changed
   git status
   
   # Add the test file
   git add test_setup.py
   
   # Commit your changes
   git commit -m "Add initial environment test script"
   
   # Push to GitHub
   git push origin main
   ```

3. **Creating a new branch** (good practice for feature development):
   ```bash
   # Create and switch to a new branch
   git checkout -b feature/data-analysis
   
   # Make changes and commit to this branch
   git add .
   git commit -m "Add data analysis functionality"
   
   # Push the branch to GitHub
   git push origin feature/data-analysis
   ```

Let me know if you need help with any specific part of this workflow!​​​​​​​​​​​​​​​​