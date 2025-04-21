# Analysis-of-the-Disk-Structure-using-Sleuth-Kit
## AIM:
To analyze the disk structure of a given disk image using Sleuth Kit tools in Kali Linux.

## DESIGN STEPS:
### Step 1:
Obtain or create a disk image file (e.g., disk.dd) to analyze. Open the terminal in Kali Linux.

### Step 2:
Use Sleuth Kit tools like mmls, fsstat, and fls to examine the partition layout, file system details, and file listing.

### Step 3:
Interpret the output of the tools to understand the disk structure, including partitions, sectors, and files.

## PROGRAM:
Sleuth Kit Disk Analysis Commands

✅ Option 1: Create a Sample Disk Image (for Testing)

Let’s create a 10MB blank disk image and simulate file system activity:

```bash
cd ~/Downloads

# Step 1: Create an empty disk image
dd if=/dev/zero of=disk.dd bs=1M count=10

# Step 2: Format it with a file system (like FAT32)
mkfs.vfat disk.dd
```

## OUTPUT:
![image](https://github.com/user-attachments/assets/7bb84d13-3c33-43d0-9f1f-c06c98f8c994)



### Create Disk

![image](https://github.com/user-attachments/assets/a286de26-1cbc-4c97-a1de-e1e5fd3dd4ec)

### mmls 
```bash
mmls disk.dd
```
### fls
```bash
fls -f fat -o 0 disk.dd
```
![image](https://github.com/user-attachments/assets/c7893c9c-f601-43cb-b6fe-fd4ca1f65aab)


![image](https://github.com/user-attachments/assets/9d3613a9-f3eb-49b6-9331-4011bcb6a7e8)

![image](https://github.com/user-attachments/assets/03d0e45f-decd-46dc-a6cd-15cd44482a01)



## RESULT:
The analysis was performed successfully using Sleuth Kit, and the disk structure was understood in detail.
