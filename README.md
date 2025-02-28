# Git LFS Integration for Large Files

## Project Description
This project demonstrates how to integrate Git LFS (Large File Storage) to handle large binary files efficiently in a Git repository.

## Table of Contents

1. Prerequisites
2. Installation Instructions
3. Usage Instructions
4. Configuration
5. Security Best Practices
6. Troubleshooting
7. Contribution Guidelines
8. License

## Prerequisites

1. Git installed on your system.
2. Git LFS installed (git-lfs package).
   1. To get the pakage for winodws refer the below link
     ``` https://git-lfs.com/ ```
   2.  For linux use below commad
     ```
          sudo apt-get install software-properties-common
          sudo add-apt-repository ppa:git-lfs/ppa
          sudo apt-get update
          sudo apt-get install git-lfs
     ```
   3. Installing Git LFS on macOS
      ``` brew install git-lfs ```

3. A GitHub repository where you have push access.

### Installation Instructions

1. Clone the repository:
``` git clone https://github.com/yourusername/git_assignment_HeroVired.git ```

2. Navigate to the project directory:
``` cd git_assignment_HeroVired ```

3. Install Git LFS:
``` git lfs install ```

## Usage Instructions
Adding Large Files to Git LFS

1. Checkout to the lfs branch:
``` git checkout lfs ```

2. Track large files using Git LFS:
``` git lfs track "*.bin" ```
(Replace *.EXE with the actual file extension of your large files.)

3. Add a large file (must be over 200MB) to the repository:
  ```
cp /path/to/largefile.bin .
git add .gitattributes largefile.bin
git commit -m "Added large file with Git LFS tracking"
git push origin lfs

```

## Verifying on Another Machine

1. Clone the repository on a different machine:
  ``` git clone https://github.com/yourusername/git_assignment_HeroVired.git ```

2. Navigate into the directory and pull the LFS files:
  ```
      cd git_assignment_HeroVired
      git lfs pull
  ```
3. Verify the large file is downloaded correctly:
  ``` ls -lh largefile.bin ```

## Configuration
Modify .gitattributes to include additional file types for Git LFS tracking if needed.

## Security Best Practices

1. Do not commit sensitive files to Git LFS.
2. Ensure Git LFS is installed before cloning repositories containing large files.
3. Regularly clean up unnecessary large files using:
  ``` git lfs prune ```

## Troubleshooting
1. Git LFS not recognized? Run:
  ``` git lfs install ```

2. Push fails due to file size limits? Check GitHub's file size limits and use a different storage method if needed.

## Contribution Guidelines

Contributions are welcome! To contribute:

1. Fork the repository.
2. Create a feature branch (feature-new-functionality).
3. Commit changes and push to your fork.
4. Submit a pull request for review.

## Example

![image](https://github.com/user-attachments/assets/a71b48a6-a0f2-4760-a8cd-e08d6f42ccc0)
