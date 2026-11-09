# Raspberry Pi LAN Radio Streaming Service - Demonstration Video at the End

A local-network radio streaming service built on a **Raspberry Pi 4 Model B**.

The project involved configuring a Linux-based audio streaming environment using **Icecast**, **DarkIce**, and a virtual audio loopback device. Downloaded music files were used as the audio source, allowing the Raspberry Pi to operate as a radio streaming server accessible to devices on the same Local Area Network (LAN).

## Project Overview

The objective was to build and configure a functional radio streaming service using a Raspberry Pi running Linux.

The Raspberry Pi hosted the Icecast streaming server, while DarkIce captured and encoded the audio input before sending it to the server. A virtual audio loopback device provided a way to route audio playback into the streaming pipeline.

The resulting stream was available to other devices connected to the same local network.

This was a **LAN-only project**, not a publicly accessible internet radio station.

## Hardware

- Raspberry Pi 4 Model B
- Monitor connected to the Raspberry Pi through a micro-HDMI-to-HDMI connection
- Second monitor connected to a separate PC for the demonstration setup
- Speaker connected to the Raspberry Pi's 3.5 mm audio jack
- microSD card containing the Linux operating system
- Network connection for LAN communication

## Software and Technologies

| Technology | Purpose |
| Linux | Operating system and environment for the radio server |
| Icecast | Audio streaming server that distributes the stream to listeners |
| DarkIce | Audio capture and encoding client that sends audio to Icecast |
| Audio loopback device | Virtual audio routing between playback and capture |
| Local music files | Audio content used as the radio source |
| LAN networking | Allows other devices on the same network to access the stream |

### Icecast

Icecast is an open-source streaming media server. It receives audio from a source client and distributes the stream to connected listeners.

In this project, Icecast acted as the central radio server hosted on the Raspberry Pi.

### DarkIce

DarkIce is a live audio streamer that captures audio from an audio interface or supported software audio source, encodes it into a streaming format, and sends it to a configured Icecast server.

It connected the audio input pipeline to the Icecast server.

### Audio Loopback Device

The virtual audio loopback device provided an internal audio-routing mechanism.

It allowed audio being played by the system to be made available as an input to the streaming software, avoiding the need to capture the audio through a physical microphone.

### LAN Networking

The service was configured for access within the local network.

Other devices connected to the same LAN could connect to the Raspberry Pi's Icecast server using its local IP address and configured streaming port.

## Audio Streaming Workflow

The general audio pipeline was:

1. Music files were stored locally on the Raspberry Pi.
2. Audio playback provided the source audio.
3. The virtual loopback device routed the playback audio to a capture input.
4. DarkIce captured and encoded the audio.
5. DarkIce transmitted the encoded stream to Icecast.
6. Icecast made the stream available to connected LAN clients.

## Hardware Setup

The Raspberry Pi was connected to a monitor using its HDMI display output and to an external speaker through its 3.5 mm audio jack.

A second monitor connected to a separate PC was used during the demonstration.

This setup allowed the Raspberry Pi system and the separate PC to be displayed independently while demonstrating the radio streaming service.

## Network Access

The radio service was intended for local-network use.

Listeners on the same network could access the Icecast server using an address in the following format:

`http://<RASPBERRY_PI_LOCAL_IP>:8000`

The exact stream URL depends on the configured Icecast mountpoint.

The service was not configured as a public internet radio station.

## Demonstration

A video demonstration of the Raspberry Pi hardware setup and radio streaming project is available here:

** https://www.youtube.com/watch?v=9OWSV__QgpE **

The video shows the Raspberry Pi 4 Model B, its monitor and speaker connections, and the physical setup used for the project.

## Skills and Learning Outcomes

This project provided practical experience with:

- Linux system configuration and administration
- Raspberry Pi hardware setup
- Audio devices and virtual audio routing
- Audio capture and encoding
- Icecast server configuration
- DarkIce source-client configuration
- LAN-based network services
- Understanding client-server communication
- Troubleshooting software and hardware integration

## Project Context

Developed as part of a Operating Systems module.

This project demonstrates the practical use of a Raspberry Pi as a lightweight Linux-based streaming server.

## Notes

- The streaming service was designed for LAN access only.
- The project used locally stored music files for demonstration.
- No music files are included in this repository.
- Any music used in a reproduced setup should be appropriately licensed or otherwise authorised for use.
- Configuration files containing passwords or other credentials should not be published.
