# Experiment No. 6: Use Sleuth Kit to Analyze Digital Evidence

## Aim

To use the Sleuth Kit command-line tools to analyze a forensic disk image, identify the file system and partitions, list files and directories, recover a file, and analyze file metadata.

## Software Used

- Sleuth Kit 4.14.0
- Windows PowerShell
- Forensic Disk Image

## Description

The Sleuth Kit (TSK) is a collection of command-line tools used for analyzing disk images and recovering digital evidence. In this experiment, the forensic disk image `4Dell Latitude CPi.E01` is analyzed using Sleuth Kit tools.

## Step 1: Install and Open Sleuth Kit

The Sleuth Kit tools were downloaded and the bin directory was opened. The bin directory contains tools such as fsstat.exe, mmls.exe, fls.exe, icat.exe, istat.exe and img_stat.exe.


<img width="1881" height="1057" alt="Screenshot 2026-09-15 094436" src="https://github.com/user-attachments/assets/39a02b5a-606a-4d8b-99b0-ccaf6b8edb8b" />



## Step 2: Identify the File System Using fsstat

The fsstat command was used to identify and analyze the file system present in the forensic image.

The output shows that the file system is NTFS and the image contains Windows XP file-system information.

<img width="1461" height="698" alt="Screenshot 2026-09-15 095244" src="https://github.com/user-attachments/assets/3cb9fd50-71c1-465b-b155-77ac225caf33" />


## Step 3: List Partitions Using mmls

The mmls command was used to identify the partition structure of the forensic disk image.

The output shows the DOS partition table and an NTFS/exFAT partition.

<img width="1473" height="275" alt="Screenshot 2026-09-15 095821" src="https://github.com/user-attachments/assets/d4daaf63-663e-4cd0-9da8-c141dd6e41fd" />


## Step 5: Recover a File Using icat

The inode number of excel.xls was identified from the file listing. The icat command was then used to recover the file from the forensic image.

The recovered file was saved as: recovered_excel.xls

<img width="480" height="599" alt="6" src="https://github.com/user-attachments/assets/d91220fc-1477-4204-94bc-258ac0f0becd" />

<img width="1448" height="62" alt="Screenshot 2026-09-15 100545" src="https://github.com/user-attachments/assets/9bfd3c26-f739-4ab8-b191-70bb43e03d6e" />


## Step 6: Analyze File Metadata Using istat

The istat command was used to analyze the metadata associated with the excel.xls file.

<img width="1455" height="691" alt="Screenshot 2026-09-15 100602" src="https://github.com/user-attachments/assets/6047b0b2-7287-434f-bbfe-635eeb2feb4b" />


## Step 7: Examine the Generated File List

The generated file_list.txt file was opened to examine the files and directories identified by Sleuth Kit.

<img width="1465" height="330" alt="Screenshot 2026-09-15 100256" src="https://github.com/user-attachments/assets/b654aed9-c084-407b-a95a-3599bf703014" />


## Step 8: Timeline Analysis (Optional)

The experiment manual specifies timeline analysis as an optional step. A body file was generated using fls.

The Sleuth Kit Windows package contains mactime.pl rather than mactime.exe. Perl was not available in the Windows environment, so the optional mactime timeline generation was not executed.

<img width="1465" height="330" alt="Screenshot 2026-09-15 100256" src="https://github.com/user-attachments/assets/4bd3a5ce-0224-442c-80ef-315f300063df" />


## Step 9: Generate and Collect the Report Data

The generated analysis files were collected.

<img width="338" height="227" alt="10" src="https://github.com/user-attachments/assets/504cb8b9-60dd-4376-ad6f-1338038c37bb" />


## Result

The forensic disk image 4Dell Latitude CPi.E01 was successfully analyzed using Sleuth Kit.

The following operations were successfully performed:

- Identified the file system as NTFS using fsstat.
- Identified the partition structure using mmls.
- Listed files and directories using fls.
- Identified the inode of excel.xls.
- Recovered excel.xls using icat.
- Analyzed file metadata using istat.
- Generated a body file for optional timeline analysis.

The recovered file was saved as: recovered_excel.xls

## Conclusion

Sleuth Kit was successfully used to analyze the forensic disk image and extract digital evidence. The experiment demonstrated file-system analysis, partition identification, file listing, file recovery, and metadata analysis using command-line forensic tools.
