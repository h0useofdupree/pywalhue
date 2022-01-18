# This is a fork from lkarbownik's pywalhue.
His version is outdated and I - as a moderate noob - wanted to try and bring this puppy back. But I really do not think this is needed anywhere, since there is no complication in this script except for pywal - which of course is not my credit. From time to time I will upgrade this script. Following is a table with stuff I added and stuff I am going to.

| Feature	| Description		| Status	|
|---------------|-----------------------|---------------|
| Setup Script  | This script will ask for the IP <br/> and give a list of lamp names <br/> to add | in progress |

# pywalhue
A simple wrapper over pywal to integrate it with Philips Hue light system

## Getting Started
### How to use
Simply run `pywalhue -i ~/file/path/to/image` to generate a new colorscheme using pywal and trigger pywal-hue-hook to send an API request to Hue Bridge API.

You can use pywal-hue-hook directly:  
Running `pywal-hue-hook.py` will load the background color from last theme generated by pywal and send it to Hue Bridge API.  
You can also test the hook by providing a specific color in the hex format as the first argument, e.g. `pywal-hue-hook.py FF00FF`

### Configuration
To configure the script you need to provide 2 variables in pywal-hue-hook.py file:
- `BRIDGE_IP` - a string specifying IP address of the bridge, e.g. `'192.168.1.30'`
- `LIGHTS` - a string or a list of strings specifying name(s) of light(s) to be used
- Optionally, you can uncomment selected line responsible for calculating brightness level based on RGB input - by default lights will be set to 100% brightness 

Also, note that before first usage of the script you may need to press a bridge button to allow for registration of new API user.

### Requirements
- `python3`
- `pywal`
- `phue`
- `rgbxy`

To install required modules cd into repo directory and run the following comand:

`pip3 install -r requirements.txt`

### Installation
Copy `pywalhue` and `pywal-hue-hook.py` to a directory listed in $PATH environment variable, e.g. `/usr/local/bin`

### Demo
[Youtube](https://www.youtube.com/watch?v=VlOteZxqEnw)
