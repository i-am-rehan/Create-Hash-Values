# 🔑 Create Hash Values

This project demonstrates the use of Linux hashing commands to generate and compare file integrity values. The activity simulates a real-world scenario where two files appear identical, but hashing is used to confirm whether their contents are truly the same or modified.

---

## 📂 Activity Overview
As a security analyst, verifying file integrity is an important step in protecting organizations from tampering and malware.  
In this activity:
- Displayed the contents of two files (`file1.txt` and `file2.txt`)
- Generated SHA-256 hash values for both files
- Compared the hashes manually and using Linux tools
- Confirmed whether the files were identical or different

---

## 🕵️ Scenario
Two suspicious files were discovered in the `/home/analyst` directory. While both appeared identical when viewed with `cat`, hashing techniques were required to validate their integrity and detect any hidden differences.

---

## ✅ Tasks Performed

### 1. Generate Hashes for Files
- Used `ls` to list available files (`file1.txt`, `file2.txt`).
- Displayed file contents with `cat` → both appeared the same.
- Generated SHA-256 hash values:
  ```
  sha256sum file1.txt
  sha256sum file2.txt
  ```
### 2. Compare Hashes

- Saved hash values into separate files:
```
sha256sum file1.txt >> file1hash
sha256sum file2.txt >> file2hash
```
- Displayed saved hashes with `cat file1hash` and `cat file2hash`.

- Compared the two hash files using:
```
cmp file1hash file2hash
```

- Output confirmed differences at the first character of line 1.

 📌 Conclusion: Despite appearing identical, the files were different at the binary level.

## 🛠️ Skills Practiced

- 🖥️ Linux command-line navigation (`ls`, `cd`, `cat`)

- 🔑 Hash generation with `sha256sum`

- 📂 File output redirection (`>>`)

- ⚖️ Manual and automated hash comparison (`cat`, `cmp`)

- 🛡️ Data integrity validation

### 📸 Screenshots

- File listing and initial inspection with `cat`

- Generated SHA-256 hash values for both files

- Comparison showing different hash outputs

- `cmp` command highlighting the difference

<img width="853" height="371" alt="image" src="https://github.com/user-attachments/assets/d8d0aa03-baef-41e4-abaf-f48d008aea1a" />


### ⚡ Conclusion

This lab provided hands-on experience with hash functions for file integrity checks. It highlighted how files that look identical can still differ internally, and how Linux tools like `sha256sum` and `cmp` are essential for security analysts to detect tampering, malware injection, or unauthorized modifications.

