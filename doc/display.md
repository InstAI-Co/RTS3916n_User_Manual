# <div align="center">How To Display Frame In The Real-Time</div>

There are two different ways to display the frames in the window, and the list below is our main method to transport the image, as follows:

- NFS
- UDP

## <div align="center">How to Start</div>

We provide another repository containing more detailed information. Inside, there is a README.md file that describes how to use these files.

<details open>
<summary>Clone</summary>

```shell
# This command will require you to enter a key to access. Please contact us, and we will provide the key for you.
git clone https://github.com/InstAI-Co/Realtek-RTS3916n-Display-Multiple-Image.git
```

After setting up the environments, you can select one of the modes to use.

</details>

<details open>
<summary>Usage</summary>

### NFS

```shell
python src/display-real-time.py path/to/stream/image/
```

Since the NFS mode will generate multiple images in the common folder, it means that when the detected frame is saved in bitmap format, the computer-side will capture the latest frame and display it in the window to simulate real-time.

### UDP

```shell
python src/udp-server.py <IP> <PORT> <RESIZE_WIDTH> <RESIZE_HEIGHT>
```

This is an efficient way to display the frames because it provides an easy interface to capture the frames sent by the Realtek EVB. It also shows low latency compared with NFS-based transport.

</details>

Congratulations! You have completed this tutorial.
