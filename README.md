
This is a fork of the work done by John Jacobsen at;

https://github.com/eigenhombre/paperproto/tree/master?tab=MIT-1-ov-file

This is a Python script to show system information for a Raspberry Pi Zero W on a Waveshare v4 e-ink Hat.


sudo apt-get install wget git python3-pip python3-pil python3-numpy python3-spidev python3-pillow python3-setuptools python3-gpiozero

git clone https://github.com/cjstoddard/epaper-status.git
cd epaper-status

Edit stat.py, look for pi_parent_dir and change the patch appropriatly. 

To Do list:
Make this work with pip install, the libraries are available at;

https://pypi.org/project/waveshare-epaper/

Not implemented yet!
git clone https://github.com/cjstoddard/epaper-status.git
cd epaper-status
python3 -m venv venv
source venv/bin/activate
pip install waveshare-epaper


Warranty:
THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.