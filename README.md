<div align="center">
  <h3 align="center">AppArmor Profiles</h3>

  <p align="center">
    AppArmor profiles for my personal computer and server
    <br />
    <a href="https://github.com/70xH/AppArmorProfs/issues">Report Bug</a>
    ·
    <a href="https://github.com/70xH/AppArmorProfs/issues">Request Feature</a>
  </p>
</div>

<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#roadmap">Roadmap</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgments">Acknowledgments</a></li>
  </ol>
</details>

## About The Project

Contains all of personal important apparmor profiles used in my system and server. This repo will always be updating to improve security of interactions between said software and the system.
There are multiple profiles out in the internet, but these profiles are implemented and improved focusing on particular preferences.

<p align="right">(<a href="#top">back to top</a>)</p>

## Getting Started

To use the same profiles, I recommend to follow the following steps:

1. As the mentioned system runs Void Linux:

```
sudo xbps-install apparmor libapparmor libapparmor-devel runit-void-apparmor
```

2. Append the following to `GRUB_CMDLINE_LINUX_DEFAULT` in `/etc/default/grub`

```
apparmor=1 security=apparmor
```

3. Set default mode to complain by changing the variable `APPARMOR` in `/etc/default/apparmor`

```
APPARMOR=complain
```

4. Clone the repository

```
git clone github.com/70xH/AppArmorProfs
```

5. Copy the files in the repo to the folder `/etc/apparmor.d/`

6. Enforce the profile rules by using `aa-enforce`. For example

```
sudo aa-enforce <program_path>
```

## Usage

This section will cover a simple example of how to write your own profile

TODO

## Contributing

Contributions are what make the open source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

If you have a suggestion that would make this better, please fork the repo and create a pull request. You can also simply open an issue with the tag "enhancement".
Don't forget to give the project a star! Thanks again!

1. Fork the Project
2. Create your Feature Branch (`git checkout -b profile/NewProfile`)
3. Commit your Changes (`git commit -m 'Add some NewProfile'`)
4. Push to the Branch (`git push origin profile/NewProfile`)
5. Open a Pull Request

<p align="right">(<a href="#top">back to top</a>)</p>

## License

Distributed under the MIT License. See `LICENSE` for more information.

<p align="right">(<a href="#top">back to top</a>)</p>
