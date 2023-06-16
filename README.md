# AppArmor profile for Thunderbird for Debian #

An AppArmor profile to confine Thunderbird.

This profile is just an extension of the upstream AppArmor Debian profile.
The upstream AppArmor upstream profile is the foundation.

Primarily this AppArmor profile makes Debian's AppArmor profile for
Thunderbird compatible with Qubes Debian based VMs.

This profile is developed by the Kicksecure team.
Thunderbird is developed by mozilla.org.

## How to install `apparmor-profile-thunderbird` using apt-get ##

1\. Download the APT Signing Key.

```
wget https://www.kicksecure.com/keys/derivative.asc
```

Users can [check the Signing Key](https://www.kicksecure.com/wiki/Signing_Key) for better security.

2\. Add the APT Signing Key.

```
sudo cp ~/derivative.asc /usr/share/keyrings/derivative.asc
```

3\. Add the derivative repository.

```
echo "deb [signed-by=/usr/share/keyrings/derivative.asc] https://deb.kicksecure.com bookworm main contrib non-free" | sudo tee /etc/apt/sources.list.d/derivative.list
```

4\. Update your package lists.

```
sudo apt-get update
```

5\. Install `apparmor-profile-thunderbird`.

```
sudo apt-get install apparmor-profile-thunderbird
```

## How to Build deb Package from Source Code ##

Can be build using standard Debian package build tools such as:

```
dpkg-buildpackage -b
```

See instructions.

NOTE: Replace `generic-package` with the actual name of this package `apparmor-profile-thunderbird`.

* **A)** [easy](https://www.kicksecure.com/wiki/Dev/Build_Documentation/generic-package/easy), _OR_
* **B)** [including verifying software signatures](https://www.kicksecure.com/wiki/Dev/Build_Documentation/generic-package)

## Contact ##

* [Free Forum Support](https://forums.kicksecure.com)
* [Premium Support](https://www.kicksecure.com/wiki/Premium_Support)

## Donate ##

`apparmor-profile-thunderbird` requires [donations](https://www.kicksecure.com/wiki/Donate) to stay alive!
