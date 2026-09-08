# Detecting-steganography-with-tools-like-StegExpose-analyzing-file-signatures
## AIM:
To detect hidden data using steganography detection tools like StegExpose and analyze file signatures for authenticity and manipulation.
## Requirements:
- **Operating System:** Linux / Windows
- **Tools:**
    - StegExpose (Java-based tool)
    - Hex Editor (e.g., xxd, HxD)
    - File command (Linux) or TrID (Windows)
- **Sample files:**
    - Suspected stego files (.jpg, .png, .wav)
    - Clean reference files
## ARCHITECTURE DIAGRAM:
```mermaid
flowchart TD
    A[Input File: JPG/PNG/WAV] --> B[File Signature Analysis]
    B --> C{Signature Match?}
    C -- Yes --> D[Pass to StegExpose]
    C -- No --> E[File Tampered / Mismatch]
    D --> F[StegExpose Detection: Suspicious or Clean]
    F --> G[Report Findings]
```

## DESIGN STEPS:
### Step 1:
Install StegExpose or use the JAR version to detect steganography in image files.

### Step 2:
Run StegExpose on a directory of suspected image files using the command:

### Step 3:
Analyze file signatures using tools like file, binwalk, or xxd to check for inconsistencies or embedded content.

## PROGRAM:
**Check file type**
```bash
file suspect.jpg
```
or view magic bytes:
```
xxd suspect.jpg | head
```
**Run StegExpose**
```bash
java -jar StegExpose.jar suspect.jpg
```
## OUTPUT:
List of Images with Steganography Detection Scores and File Signature Details
<img width="1595" height="522" alt="image" src="https://github.com/user-attachments/assets/70b91af3-9006-4169-b897-83377d9350fc" />


<img width="906" height="252" alt="image" src="https://github.com/user-attachments/assets/127d99d7-edf1-4db5-96a4-5f5d4e4456e5" />

<img width="892" height="466" alt="image" src="https://github.com/user-attachments/assets/7aab44cf-a015-4359-8b8e-8d811d658e49" />

## RESULT:
Hidden data was successfully detected and file signatures were analyzed for irregularities.
