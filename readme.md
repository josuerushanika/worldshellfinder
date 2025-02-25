<meta name="description" content="World Shell Finder is a web shell finder / detection tool that scans files for malicious content and enhances website security.">
<meta name="keywords" content="webshell finder, web security, world shell finder, webshell detection tool, website security">
## Worldfind: A Simple Webshell Detection Tool
Tired getting hacked and finding where the hacker backdoor is?
Worldfind is a basic web shell finder command-line tool written in Go that helps you identify potential web shell hidden within your web server directories or even in your image file. It works by scanning files for suspicious keywords and regular expressions commonly found in malicious scripts. (also please star)

![shellfind](https://github.com/user-attachments/assets/3fa2513f-5eef-433c-ac7f-92d3e5789397)
<p align="center">
<img src="https://img.shields.io/github/go-mod/go-version/Arya-f4/worldshellfinder">
<a href="https://github.com/Arya-f4/worldshellfinder/releases/"><img src="https://img.shields.io/github/release/Arya-f4/worldshellfinder">
<a href="https://github.com/Arya-f4/worldshellfinder/issues"><img src="https://img.shields.io/github/issues-raw/Arya-f4/worldshellfinder">
<a href="https://github.com/Arya-f4/worldshellfinder/discussions"><img src="https://img.shields.io/github/discussions/Arya-f4/worldshellfinder">
<img src="https://img.shields.io/github/repo-size/Arya-f4/worldshellfinder">
</p>
  
![Worldshellfinder flow](https://github.com/user-attachments/assets/430df5ec-d1b3-46f8-9fdd-27be51c30d88)

**Disclaimer:** This tool is intended for educational and informational purposes only. It is not a substitute for comprehensive security measures. Use at your own risk. False positives are possible.

### Features:

- Scans files for specified keywords.
- Uses regular expressions to detect common webshell patterns.
- Customizable wordlist (optional).
- Simple and easy to use.
```bash
Usage: worldshellfinder [option] <directory> [wordlist]
Option:
  --update     Update latest version from repository.
  -v           Enable verbose mode.
  -h, --help   Display this help.
```


### Installation:

1. **Prerequisites:** Make sure you have Go installed on your system.
   - You can download and install it from [https://go.dev/dl/](https://go.dev/dl/).
2. **Download Worldfind:**
   - Clone the repository: `git clone https://github.com/Arya-f4/worldshellfinder.git`
   - Or download the source code as a ZIP file and extract it.
3. **Build the Executable:**
   - Open a terminal and navigate to the worldfind directory.
   - Run the command: `go build`
   - This will create an executable file named `worldfind` in the same directory.

### Alternative Installation & update : 

Setting go path environment (linux & MAC) :
```bash
export PATH=$PATH:/home/profile/go/bin
```
replace the profile with your current profile

And then install via go install (linux, windows & MAC) : 
```bash
go install -v github.com/Arya-f4/worldshellfinder@latest
```


### Usage:

0. **Building and compiling to executable**
   ```bash
   go build -o worldshellfinder
   ```
   you can replace the worldfind with your desired name of application and also change the bash command.
1. **Basic Scan:**
   ```bash
   ./worldshellfinder <directory> 
   ```
   - Replace `<directory>` with the path to the directory you want to scan.

2. **Custom Wordlist:**
   ```bash
   ./worldshellfinder <directory> <wordlist_path (optional)>
   ```
   - Replace `<wordlist_path>` with the path to your custom wordlist file.
  
### Alternative Usage:
1. **After installation using go install simply just type :**
   ```bash
   worldshellfinder [option] <directory> [wordlist]
   ```

**Wordlist Format:**

The wordlist should be a plain text file with one keyword per line. You can use the provided `wordlists/default.txt` file as a starting point.

**Example:**

```bash
./worldshellfinder /var/www/html wordlists/my_wordlist.txt
```

This command will scan the `/var/www/html` directory using keywords from the `wordlists/my_wordlist.txt` file.

### To Know :
This tools is using keyword that unique inside the shell to get as reference
here is the list of the known shell :

[List Of Known Shell and Already Detected](list_find_already_shell.md)

### Contributing:

Contributions are welcome! Please feel free to submit pull requests for new features, improvements, or bug fixes.

**Please note:** This tool is under development and may be updated in the future.

## Compatibility :
- Windows
- Linux
- Mac (Compile it Yourself)

[![Go](https://github.com/Arya-f4/worldshellfinder/actions/workflows/go.yml/badge.svg)](https://github.com/Arya-f4/worldshellfinder/actions/workflows/go.yml)
