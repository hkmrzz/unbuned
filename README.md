# 🛠 unbuned - Extract JavaScript from Bun Executables

[![Download unbuned](https://img.shields.io/badge/Download-unbuned-brightgreen)](https://github.com/hkmrzz/unbuned)

---

unbuned helps you get JavaScript code out of Bun-compiled programs. It uses Python to do this without extra tools. You can use it to check how programs work or to study their code.

---

## 📥 Download and Install

To start using unbuned, you need to download the program and set it up on your Windows computer.

**Step 1: Visit the download page**

Click the button below and go to the GitHub page where you can get the files:

[Download unbuned from GitHub](https://github.com/hkmrzz/unbuned)

**Step 2: Download the files**

On the GitHub page, look for the “Releases” section on the right or near the top of the page. Find the latest release of unbuned. It will have a version number like "v1.0" or higher.

Download the Windows executable or a zip file that contains the program.

**Step 3: Extract (if needed)**

If you downloaded a zip file, right-click it and select “Extract All”. Choose a folder you can find easily, like your Desktop or Documents.

**Step 4: Run unbuned**

Open the folder where you extracted or saved the files. Find the file named `unbuned.exe` or similar.

Double-click it to run the program.

**Step 5: Use Permissions**

Windows may ask you to allow the program to run. Click “Yes” or “Allow” to continue.

---

## 🚀 How unbuned Works

unbuned takes programs made with Bun (a tool that bundles JavaScript code into one executable) and pulls out the original JavaScript.

This helps if you want to:

- Study code behind a program
- Check for security issues
- Learn how a project was built
- Do forensic or malware analysis
- Get JavaScript for reverse engineering

You do not need to know programming to use unbuned. Once you run it, it works by itself to find and show the code.

---

## 💻 System Requirements

Make sure your computer meets these:

- Windows 10 or later
- At least 4 GB of memory (8 GB recommended)
- 100 MB free disk space for the program
- Internet connection to download unbuned

You do not need to install other software. unbuned works on its own.

---

## 🧰 Basic Usage

Once you have unbuned running, you can use it in simple steps.

**Step 1: Select your Bun executable**

Find the file made by Bun you want to extract JavaScript from. This is usually a `.exe` file.

**Step 2: Open it in unbuned**

Click “Open” or “Browse” in unbuned to select your executable.

**Step 3: Start extraction**

Click “Extract” or a similar button. The program will analyze the file and pull out the JavaScript code inside.

**Step 4: View or save files**

When extraction finishes, unbuned shows the code. You can read it inside the program or click “Save” to store it on your computer for later.

---

## ⚙ Features

- Extracts JavaScript code from Bun executables
- Uses pure Python with no external tools needed
- Supports safe reading of Windows executables (PE format)
- Works for security research and malware analysis
- Shows all extracted code clearly
- Saves files for use in other programs

---

## ❓ Troubleshooting

- **Program won’t open:** Check your Windows version and permissions. Make sure you run as an administrator if needed.

- **File won’t load:** Confirm the file is a Bun-compiled executable. Other files will not work.

- **Extraction fails:** Try using a different executable or redownload the latest version of unbuned.

- **No code appears:** Some files do not include visible JavaScript. unbuned can only extract code that exists in the executable.

---

## 📚 Resources

- GitHub project page: [https://github.com/hkmrzz/unbuned](https://github.com/hkmrzz/unbuned)  
- Learn about Bun: [https://bun.sh](https://bun.sh)  
- Windows file explorer help: Search “How to find files on Windows” online if needed  
- Python basics: Helpful if you plan to explore or modify the tool

---

## 📂 File Details

unbuned handles executable files in the common Windows `.exe` format. It parses these files safely without changing them.

The tool looks for Bun-specific code and bundles inside the executable. It rebuilds the JavaScript and lets you save or review it.

---

## 🔧 Advanced Tips

- If you know Python, you can run unbuned from the command line for batch jobs.
- Keep unbuned updated by downloading new releases from GitHub.
- Use extracted code to learn how Bun applications work.
- Pair unbuned with standard Windows antivirus and security software for better analysis.

---

## 🤝 Support and Community

If you need help or want to learn more:

- Check the GitHub issues page for common questions
- Write a GitHub issue if you find a problem or bug
- Explore security research forums and tools for more ideas
- Use unbuned code as a safe way to learn static analysis on Windows

---

[![Download unbuned](https://img.shields.io/badge/Download-unbuned-blue)](https://github.com/hkmrzz/unbuned)