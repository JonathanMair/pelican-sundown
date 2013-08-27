# Pelican-Sundown

A flexible [pelican](http://docs.getpelican.com) based on the [github
pages](https://github.com/orderedlist) sundown theme created originally by [orderedlist](http://pages.github.com/).

## Configuration

This theme does have a few differences from the original sundown theme.
For example, slightly larger font for content, gravatar image, and
social icons.

Additions such as gravatar are not required, but available.  The
following settings should be added/adjusted in the `pelicanconf.py`:

### Gravatar

You can include a gravatar image in the top left of the template by
adding the following lines to your config:

```python
import urllib, hashlib

# Conf for pulling Gravatar Image
EMAIL = u'youremail@email.com'
DEFAULT_GRV_URL = u'http://www.example.com/default.jpg'
GRV_SIZE = 120

# construct gravatar URL
GRV_URL = "http://www.gravatar.com/avatar/" + hashlib.md5(EMAIL.lower()).hexdigest() + "?"
GRV_URL += urllib.urlencode({'d':DEFAULT_GRV_URL, 's':str(GRV_SIZE)})
``` 

## Who is using pelican-sundown

* [KenIngle.com](http://keningle.com) - Hosted on github pages
 
## License (MIT)

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
