
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

Edit stat.py and look for the line that reads;

> if hostname == "pi-zero-1":

Change pi-zero-1 to the host name of your device, then save and exit. Once that is done, you should be able to run the program with; 

> python3 stat.py

Notes:

In the code there is a check for the hostname that is hard coded. The hard coded hostname must be changed in order for this program to work properly. This was done by the original author for testing purposes so he could run the program on his development machine before running it on his Raspberry Pi. I have chosen to keep the code in the program because it was actually kind of a clever way to handle it. If you want to shorten the program, removing the is_pi checks is a good way to do it.

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