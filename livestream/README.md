Instructions for Livestreaming and Video Publishing 
===================================================

## Before Meetup

- [ ] Obtain consent for recording and livestreaming from Speakers
- [ ] Obtain credentials to publish to [live.mesh.world](https://live.mesh.world) by asking on [#meshtv:tomesh.net](https://chat.tomesh.net/#/room/#meshtv:tomesh.net)
- [ ] Configure [OBS Studio](https://obsproject.com) on your system and the Profile and Scene in this repository (you will need to change some local paths in your Sources after the import)
- [ ] Connect to the streaming server by:
  - Authenticate with OpenVPN credentials obtained earlier
  - Press `Start Streaming` and visit [https://live.mesh.world](https://live.mesh.world) to verify streaming (with up to 2 min latency)
  - **Important**: If stream does not start, you need to SSH into `live.mesh.world` and restart the process using `sudo systemctl restart process-stream.service`, people at [#meshtv:tomesh.net](https://chat.tomesh.net/#/room/#meshtv:tomesh.net) should be able to help with that
  - Press `Start Recording` and verify the `mp4` file recorded to your local device
- [ ] Obtain [Our Networks Twitter account](http://twitter.com/_ournetworks) credentials or arrange someone who can do that

## During Meetup

- [ ] Arrive half an hour early
- [ ] Verify that Speakers are comfortable for livestreaming and recording
- [ ] Find a suitable spot where you can see the Speaker and the slides, and pick up good audio from the area
- [ ] Set up laptop:
  - Ensure stable connection (ideally wired ethernet)
  - Connect to OpenVPN (you should then be able to `ping openvpn.publish.live.mesh.world` at `10.10.10.1`)
  - Open up OBS Studio and test `Start Streaming` and `Start Recording` as before
  - Leave the laptop streaming and locally recording
- [ ] Send tweet to announce livestream availability on `https://live.mesh.world`, include presentation topic and speaker information in tweet
- [ ] After presentation, stop the streaming and recording, then close OBS Studioa and disconnect from OpenVPN

## After Meetup

- [ ] Do any post-processing of the locally recording `mp4` file necessary
- [ ] Upload to IPFS and pin it on [ipfs.io](https://ipfs.io) using [IPFS Pinbot](https://twitter.com/ipfspin) by tweeting:
  ```
  @ipfspin !pin IPFS_CONTENT_HASH
  ```
- [ ] Verify video playback at `https://ournetworks.ca/video/?ipfs=IPFS_CONTENT_HASH`
- [ ] Tweet the link with presentation topic and speaker information in tweet
