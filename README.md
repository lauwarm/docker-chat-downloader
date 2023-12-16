# Docker Chat Downloader

## Overview

Docker Chat Downloader is a Dockerized version of the [Chat Downloader tool](https://github.com/xenova/chat-downloader), allowing users to easily download chat logs from various streaming platforms. This containerized solution simplifies the deployment process and ensures a consistent environment for running the Chat Downloader.

## Prerequisites

- Docker installed on your system.

## Quick Start

```bash
docker run -v /path/to/download/:/home/download/ -e channelURL='https://www.twitch.tv/twitch' -e channelName='twitch' -e uid='1000' -e gid='1000' ghcr.io/lauwarm/docker-chat-downloader:main
```

### Usage

`/home/download` - the place where the vods will be saved. Mount it to a desired place with -v option.

`channelURL` - the url of the stream you want to record.

`channelName` - the name for the stream.

`uid` - UserID, map to your desired User ID (fallback to 9001)

`gid` - GroupID, map to your desired Group ID (fallback to 9001)

The File will be saved as `streamName-YearMonthDate-HourMinuteSecond.json`

## Issues and Contributions

If you encounter any issues or have suggestions for improvements, please create an issue. Contributions are welcome!

## License

This project is licensed under the MIT License - see the LICENSE file for details.

---

**Note**: The Docker Chat Downloader is based on the [Chat Downloader project](https://github.com/xenova/chat-downloader/) by [xenova](https://github.com/xenova). All credit for the Chat Downloader tool goes to the original author.
