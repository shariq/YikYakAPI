# Yik Yak API

This is a Python implementation of the private Yik Yak API.

It can easily be shadow banned because it does not mimic iOS device requests 100% (but it theoreitcally could) and it doesn't generate real-looking locations (but it theoretically could).

## Example Usage

``` python
from yikyak import YikYakAPI

yyapi = YikYakAPI(None, 37.427367, -122.169982)
yyapi.registerUser()
messageID = yyapi.sendMessage('test').get('yakID', None)

for x in range (0, 140):
	yyapi = YikYakAPI(None, 0, 0)
	yyapi.registerUser()
	print yyapi.likeMessage(messageID)
```

## License

YikYakAPI is available under the GNU General Public License v3. See the LICENSE file for more info.
