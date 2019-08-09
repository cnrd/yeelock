# Unlock values
These are 4 different unlocks using the same phone and same lock.

* `01505c84ff2f0099cf13d74d5b246c38eb6cf702`
* `01505c85028d0085c9d5a63ea4da470ce50688c6`
* `01505c85029800f74dae629a1da681d98164a5c8`
* `01505c8502a0009011e29d3b60c7cad22d5f3119`

It seems like the first 3 bytes are always the same: `01505c`

As observed by sasicol, bytes 3,4,5,6 is a timestamp in epoch time:

* `5c84ff2f = 1552219951 = Sunday, March 10, 2019 12:12:31 PM`
* `5c85028d = 1552220813`

~~Which means that the payload differs on the remaining 17 bytes.~~

With this new information we need to identify the last 14 bytes:

* `0099cf13d74d5b246c38eb6cf702`
* `0085c9d5a63ea4da470ce50688c6`
* `00f74dae629a1da681d98164a5c8`
* `009011e29d3b60c7cad22d5f3119`

The first unlock was done a couple of minutes before the next 3, which were done in a row.

# Random observations
* The app does not seem to work without internet, as such it may even be getting the payload from a server.
* Locks are named as EL_[SERIAL_NUMBER].
* Setting up the lock in the app requires a QR code pointing to a URL: https://mp.yeeloc.com/add?data=NKmSfxkFYgqrrbwY
* The QR sticker also has a serial number on it: B0PUmFAH
* It is unknown how these are connected. (My guess is that the url is somehow encoding the Serial number and is using it to find the lock).
