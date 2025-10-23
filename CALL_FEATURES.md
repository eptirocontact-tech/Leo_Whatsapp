# 📞 Voice & Video Calling Feature Guide

## Overview

Your WhatsApp Clone now includes **real-time voice and video calling** using WebRTC technology! Make crystal-clear audio and video calls with your contacts directly through the web browser.

## Features

### Voice Calls 📞
- **One-click calling** - Click the phone icon to start a voice call
- **Mute/Unmute** - Control your microphone during the call
- **Call timer** - See how long you've been talking
- **Clear audio** - High-quality audio using WebRTC

### Video Calls 📹
- **Face-to-face** - See your contact while talking
- **Camera control** - Turn your camera on/off during the call
- **Picture-in-picture** - See yourself in a small window
- **Mute option** - Mute audio during video calls
- **Responsive layout** - Works on desktop and mobile

## How to Use

### Starting a Call

1. **Open a chat** with a contact
2. **Click the call button** in the chat header:
   - 📞 = Voice Call
   - 📹 = Video Call
3. **Wait for response** - Your contact will see an incoming call notification

### Receiving a Call

1. **Incoming call notification** appears with:
   - Contact name
   - Call type (voice or video)
2. **Choose action:**
   - ✅ Accept - Answer the call
   - ❌ Decline - Reject the call

### During a Call

**Voice Call Controls:**
- 🎤 **Mute/Unmute** - Toggle microphone
- 📵 **End Call** - Hang up

**Video Call Controls:**
- 🎤 **Mute/Unmute** - Toggle microphone
- 📹 **Video On/Off** - Toggle camera
- 📵 **End Call** - Hang up

### Ending a Call

- Click the **red phone button** (📵) to end the call
- The call will also end if either person closes their browser tab

## Technical Details

### Technology Used

- **WebRTC** - Real-time communication protocol
- **Socket.io** - Signaling for call setup
- **STUN Servers** - Google's public STUN servers for NAT traversal
- **Peer-to-peer** - Direct connection between users for best quality

### Browser Permissions

The first time you make a call, your browser will ask for permissions:

**Voice Call:**
- 🎤 Microphone access

**Video Call:**
- 🎤 Microphone access
- 📷 Camera access

**Important:** You must grant these permissions for calls to work!

### Supported Browsers

✅ **Fully Supported:**
- Chrome 74+
- Firefox 66+
- Edge 79+
- Safari 12.1+
- Opera 62+

❌ **Not Supported:**
- Internet Explorer
- Older browser versions

### Network Requirements

- **Stable internet connection** - Minimum 1 Mbps for voice, 2 Mbps for video
- **Low latency** - Best with <100ms ping
- **Firewall** - May need to allow WebRTC traffic
- **NAT** - STUN servers help with most NAT configurations

## Troubleshooting

### "Could not access camera/microphone"

**Solutions:**
1. Check browser permissions:
   - Click the 🔒 or 🛈 icon in the address bar
   - Allow microphone/camera access
2. Check if another app is using the camera/microphone
3. Try restarting your browser

### "Call failed to connect"

**Solutions:**
1. Check your internet connection
2. Ensure the other person is online
3. Try refreshing the page and calling again
4. Check if your firewall is blocking WebRTC

### "No audio/video"

**Solutions:**
1. Check if you're muted (🔇 button is red)
2. Check if video is disabled (📹 button is red)
3. Verify your microphone/camera is working in other apps
4. Check browser permissions
5. Try plugging in headphones

### "Other person can't hear/see me"

**Solutions:**
1. Check your mute/video status
2. Ask them to check their audio output
3. Ensure you granted microphone/camera permissions
4. Try ending and restarting the call

### "Call quality is poor"

**Solutions:**
1. Close other bandwidth-heavy apps
2. Move closer to your WiFi router
3. Try using a wired connection
4. Ask others on your network to pause downloads

## Privacy & Security

### What We Track
- ✅ Call events (started, ended) for system logs
- ✅ Call duration displayed to you
- ❌ **We do NOT record or store:**
  - Audio content
  - Video content
  - Call recordings

### Peer-to-Peer Connection
- Calls are **direct between users** (peer-to-peer)
- Audio/video does **not go through our server**
- Only signaling data goes through the server
- This provides better quality and privacy

### Encryption
- WebRTC uses **DTLS-SRTP** encryption
- All audio/video is encrypted end-to-end
- Only you and your contact can see/hear each other

## Testing the Feature

### Test with 2 Browser Tabs

1. **Tab 1:** Login as `Leo`
2. **Tab 2:** Login as `Owen` (in new tab or incognito)
3. **Both:** Add each other as contacts
4. **Leo:** Open chat with Owen
5. **Leo:** Click 📞 or 📹 to call
6. **Owen:** See incoming call, click Accept ✅
7. **Both:** Enjoy the call!

### Test Video Call

1. Follow steps above but click 📹 instead of 📞
2. Grant camera and microphone permissions
3. You should see your own video (small window)
4. You should see the other person's video (large window)
5. Try toggling camera on/off with the 📹 button

### Test Mute Feature

1. During a call, click the 🎤 button
2. Button turns red (🔇) when muted
3. Other person can't hear you
4. Click again to unmute

## Known Limitations

1. **No group calls** - Currently supports 1-on-1 calls only
2. **No call history** - Calls are not logged (for privacy)
3. **No call recording** - Cannot record calls
4. **Browser only** - No mobile app (yet)
5. **Requires HTTPS in production** - WebRTC requires secure connections

## Future Enhancements

Potential features for future versions:

- 📋 Call history log
- 🔔 Custom ringtones
- 📱 Screen sharing
- 👥 Group calls (3+ people)
- 💾 Call recording (with consent)
- 🔊 Better audio/video quality controls
- 📲 Mobile app support
- 🌐 Better NAT traversal (TURN servers)

## FAQs

**Q: Is this really free calling?**
A: Yes! It's peer-to-peer, so no charges for the call itself. You only use your internet data.

**Q: Can I call someone who's not in my contacts?**
A: No, you can only call your approved contacts for privacy and security.

**Q: Does it work on mobile?**
A: Yes, in mobile browsers (Chrome, Safari). No dedicated app yet.

**Q: Can I use it without a camera for video calls?**
A: Yes, you can turn off your camera during a video call, but you'll need to grant camera permission first.

**Q: What happens if my internet drops during a call?**
A: The call will end automatically. You'll need to call again when your connection is restored.

**Q: Can someone join my call without permission?**
A: No, calls are 1-on-1 and private. Only the person you call can answer.

## Support

If you encounter issues:

1. Check this troubleshooting guide
2. Check browser console for errors (F12)
3. Try in a different browser
4. Ensure your browser is up-to-date
5. Check your internet connection speed

---

**Enjoy your new calling feature!** 📞📹
