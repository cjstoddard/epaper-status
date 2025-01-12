
This is a fork of the work done by John Jacobsen at;

https://github.com/eigenhombre/paperproto/tree/master?tab=MIT-1-ov-file

This is a Python script to show system information for a Raspberry Pi Zero W on a Waveshare v4 e-ink Hat. This fork also contains the Waveshare edp python libraries from;

https://github.com/waveshare/e-Paper.git

To use this program you will need a Raspberry Pi Zero W, with the Raspberry Pi OS, and a properly installed Waveshare e-ink v4 Pi Hat. Once you have that you can log into the system terminal and begin the installation.


> sudo apt-get install wget git python3-pip python3-pil python3-numpy python3-spidev python3-pillow python3-setuptools python3-gpiozero
> 
> git clone https://github.com/cjstoddard/epaper-status.git
> 
> cd epaper-status
>
> python3 eink-stat.py

Once you are done testing it and making sure it works, edit the stat.sh file and change the path of this program for your environment. the to run this program at startup and rerun the program periodically, type;

> chmod +x stat.sh
> 
> sudo crontab -e

and add these lines to the file;

> @reboot /home/chris/epaper-status/stat.sh >&1

> */10 * * * * /home/chris/epaper-status/stat.sh >&1

Be sure to alter the path appropriately, then save and exit the file.

Notes:

I have altered the lib files somewhat from the originals provided by Waveshare. One of the things I changed was the default orientation of the screen. My preference is to have the USB ports on the top, if you would like them on the bottom, do this;

> nano lib/waveshare_epd/epd2in13_V4.py

Look for this line;

> img = img.rotate(270, expand=True).convert('1')

and change it to this;

> img = img.rotate(90, expand=True).convert('1')

__________________________________
To Do list:

Make this work with pip install, the libraries are available at;

https://pypi.org/project/waveshare-epaper/

Not implemented yet!

> git clone https://github.com/cjstoddard/epaper-status.git
> 
> cd epaper-status
> 
> python3 -m venv venv
> 
> source venv/bin/activate
> 
> pip install waveshare-epaper

__________________________________
Warranty:
THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.