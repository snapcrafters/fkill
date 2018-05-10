<h1 align="center">
  <img width="360" src="https://rawgit.com/sindresorhus/fkill/master/media/logo.svg" alt="fkill">
  <br />
  fkill
</h1>

<p align="center"><b>This is the snap for fkill</b>, <i>"Fabulously kill processes. Cross-platform."</i>. It works on Ubuntu, Fedora, Debian, and other major Linux
distributions.</p>

<p align="center">
<a href="https://build.snapcraft.io/user/snapcrafters/fkill"><img src="https://build.snapcraft.io/badge/snapcrafters/fkill.svg" alt="Snap Status"></a>
</p>

## Install

    snap install fkill
    snap connect fkill:process-control :process-control
    snap connect fkill:system-observe :system-observe

### Known Issues

  * AppArmor denials

```
May 10 01:00:13 skull kernel: [314823.630201] audit: type=1400 audit(1525910413.519:16937): apparmor="DENIED" operation="open" profile="snap.fkill.fkill" name="/proc/1/attr/current" pid=23322 comm="ss" requested_mask="r" denied_mask="r" fsuid=1000 ouid=0
May 10 01:00:13 skull kernel: [314823.630203] audit: type=1400 audit(1525910413.519:16938): apparmor="DENIED" operation="open" profile="snap.fkill.fkill" name="/proc/2/attr/current" pid=23322 comm="ss" requested_mask="r" denied_mask="r" fsuid=1000 ouid=0
May 10 01:00:13 skull kernel: [314823.630205] audit: type=1400 audit(1525910413.519:16939): apparmor="DENIED" operation="open" profile="snap.fkill.fkill" name="/proc/4/attr/current" pid=23322 comm="ss" requested_mask="r" denied_mask="r" fsuid=1000 ouid=0
May 10 01:00:13 skull kernel: [314823.630206] audit: type=1400 audit(1525910413.519:16940): apparmor="DENIED" operation="open" profile="snap.fkill.fkill" name="/proc/6/attr/current" pid=23322 comm="ss" requested_mask="r" denied_mask="r" fsuid=1000 ouid=0
May 10 01:00:13 skull kernel: [314823.630208] audit: type=1400 audit(1525910413.519:16941): apparmor="DENIED" operation="open" profile="snap.fkill.fkill" name="/proc/7/attr/current" pid=23322 comm="ss" requested_mask="r" denied_mask="r" fsuid=1000 ouid=0
May 10 01:00:13 skull kernel: [314823.630209] audit: type=1400 audit(1525910413.519:16942): apparmor="DENIED" operation="open" profile="snap.fkill.fkill" name="/proc/8/attr/current" pid=23322 comm="ss" requested_mask="r" denied_mask="r" fsuid=1000 ouid=0
May 10 01:00:13 skull kernel: [314823.630213] audit: type=1400 audit(1525910413.519:16943): apparmor="DENIED" operation="open" profile="snap.fkill.fkill" name="/proc/9/attr/current" pid=23322 comm="ss" requested_mask="r" denied_mask="r" fsuid=1000 ouid=0
May 10 01:00:13 skull kernel: [314823.630242] audit: type=1400 audit(1525910413.519:16944): apparmor="DENIED" operation="open" profile="snap.fkill.fkill" name="/proc/10/attr/current" pid=23322 comm="ss" requested_mask="r" denied_mask="r" fsuid=1000 ouid=0
May 10 01:00:13 skull kernel: [314823.630250] audit: type=1400 audit(1525910413.519:16945): apparmor="DENIED" operation="open" profile="snap.fkill.fkill" name="/proc/11/attr/current" pid=23322 comm="ss" requested_mask="r" denied_mask="r" fsuid=1000 ouid=0
May 10 01:00:13 skull kernel: [314823.630257] audit: type=1400 audit(1525910413.519:16946): apparmor="DENIED" operation="open" profile="snap.fkill.fkill" name="/proc/12/attr/current" pid=23322 comm="ss" requested_mask="r" denied_mask="r" fsuid=1000 ouid=0
```

([Don't have snapd installed?](https://snapcraft.io/docs/core/install))
![fkill](https://raw.githubusercontent.com/sindresorhus/fkill-cli/master/screenshot.gif "fkill")

<p align="center">Published for <img src="http://anything.codes/slack-emoji-for-techies/emoji/tux.png" align="top" width="24" /> with :gift_heart: by Snapcrafters</p>

## Remaining tasks

Snapcrafters ([join us](https://forum.snapcraft.io/t/join-snapcrafters/1325)) 
are working to land snap install documentation and
the [snapcraft.yaml](https://github.com/snapcrafters/fork-and-rename-me/blob/master/snap/snapcraft.yaml)
upstream so fkill can authoritatively publish future releases.

  - [x] Fork the [Snapcrafters template](https://github.com/snapcrafters/fork-and-rename-me) repository to your own GitHub account.
    - If you have already forked the Snapcrafter template to your account and want to create another snap, you'll need to use GitHub's [Import repository](https://github.com/new/import) feature because you can only fork a repository once.
  - [x] Rename the forked Snapcrafters template repository
  - [x] Update logos and references to `[Project]` and `[my-snap-name]`
  - [x] Create a snap that runs in `devmode`
  - [x] Register the snap in the store, **using the preferred upstream name**
  - [x] Add a screenshot to this `README.md`
  - [x] Publish the `devmode` snap in the Snap store edge channel
  - [x] Add install instructions to this `README.md`
  - [x] Update snap store metadata, icons and screenshots
  - [x] Convert the snap to `strict` confinement, or `classic` confinement if it qualifies
  - [x] Publish the confined snap in the Snap store beta channel
  - [x] Update the install instructions in this `README.md`
  - [x] Post a call for testing on the [Snapcraft Forum](https://forum.snapcraft.io) - [link](https://forum.snapcraft.io/t/call-for-testing-fkill/3021/4)
  - [-] Ask a [Snapcrafters admin](https://github.com/orgs/snapcrafters/people?query=%20role%3Aowner) to fork your repo into github.com/snapcrafters, transfer the snap name from you to snapcrafters, and configure the repo for automatic publishing into edge on commit
  - [x] Add the provided Snapcraft build badge to this `README.md`
  - [x] Publish the snap in the Snap store stable channel
  - [x] Update the install instructions in this `README.md`
  - [-] Post an announcement in the [Snapcraft Forum](https://forum.snapcraft.io)
  - [ ] Submit a pull request or patch upstream that adds snap install documentation
  - [ ] Submit a pull request or patch upstream that adds the `snapcraft.yaml` and any required assets/launchers - [link]()
  - [ ] Add upstream contact information to the `README.md`
  - If upstream accept the PR:
    - [ ] Request upstream create a Snap store account
    - [ ] Contact the Snap Advocacy team to request the snap be transferred to upstream
  - [-] Ask the Snap Advocacy team to celebrate the snap

If you have any questions, [post in the Snapcraft forum](https://forum.snapcraft.io).

<!-- 
## The Snapcrafters

| [![Your Name](http://gravatar.com/avatar/bc0bced65e963eb5c3a16cab8b004431/?s=128)](https://github.com/yourname/) |
| :---: |
| [Your Name](https://github.com/yourname/) |
--> 

<!-- Uncomment and modify this when you have upstream contacts
## Upstream

| [![Upstream Name](http://gravatar.com/avatar/bc0bced65e963eb5c3a16cab8b004431?s=128)](https://github.com/upstreamname) |
| :---: |
| [Upstream Name](https://github.com/upstreamname) |
-->
