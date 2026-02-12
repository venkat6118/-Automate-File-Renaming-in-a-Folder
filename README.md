# -Automate-File-Renaming-in-a-Folder
• Write a script that renames files in a folder with a naming pattern like file_1.txt, file_2.txt • Use os module to access file names
import os

# Path to the folder (CHANGE this to your folder path)
folder_path = "your_folder_path_here"

# Get list of files
files = os.listdir(folder_path)

# Counter for naming
count = 1

for file_name in files:
    # Get full file path
    old_path = os.path.join(folder_path, file_name)
    
    # Skip directories
    if os.path.isfile(old_path):
        
        # Get file extension (.txt, .jpg, etc.)
        extension = os.path.splitext(file_name)[1]
        
        # New file name
        new_name = f"file_{count}{extension}"
        new_path = os.path.join(folder_path, new_name)
        
        # Rename file
        os.rename(old_path, new_path)
        
        print(f"Renamed: {file_name} → {new_name}")
        count += 1

print("✅ All files renamed successfully!")

Output:
A module you have imported isn't available at the moment. It will be a
