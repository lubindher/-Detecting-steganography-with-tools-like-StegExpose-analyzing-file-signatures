# Detecting-steganography-with-tools-like-StegExpose-analyzing-file-signatures
# Lubindher S
# 212222240056
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
<img width="944" height="1018" alt="Screenshot 2025-09-27 140658" src="https://github.com/user-attachments/assets/9e86a6f5-6352-4a0d-ac68-ebd9a4d5c8b5" />

<img width="958" height="1020" alt="Screenshot 2025-09-27 140846" src="https://github.com/user-attachments/assets/63f5966a-8205-42ce-81a0-47974b6dea07" />

<img width="945" height="1015" alt="Screenshot 2025-09-27 142058" src="https://github.com/user-attachments/assets/d8563e01-0422-43a7-b2c3-4839cf44d0b3" />

<img width="947" height="1003" alt="Screenshot 2025-09-27 142203" src="https://github.com/user-attachments/assets/5db734fb-1086-4d23-9c24-c094e41af0fa" />

<img width="955" height="1025" alt="Screenshot 2025-09-27 142220" src="https://github.com/user-attachments/assets/5c067816-3c90-4ac1-a452-b773d227bf76" />
<img width="1919" height="1022" alt="Screenshot 2025-09-27 142606" src="https://github.com/user-attachments/assets/b6b461c8-48b0-48cf-926a-49e79e57b003" />
<img width="824" height="96" alt="Screenshot 2025-09-27 142815" src="https://github.com/user-attachments/assets/b63c2a9d-f29f-4037-a124-5aa2a64b743e" />

<img width="814" height="161" alt="Screenshot 2025-09-27 142900" src="https://github.com/user-attachments/assets/a89a4112-a1d2-4405-afe1-bdb14c1c6faf" />

List of Images with Steganography Detection Scores and File Signature Details

## RESULT:
Hidden data was successfully detected and file signatures were analyzed for irregularities.
