# Automated NOAA Weather Satellite Ground Station
![NOAA Weather Satellite GS](https://github.com/Sayapatri/RTL-SDR-Satellite-Weather-Station/blob/main/img/Emcwci4U0AEnE2g.jpg)
## Overview

In this project, you'll create a fully automated ground station to receive and decode NOAA weather satellite images and upload them to a website hosted on an AWS S3 bucket. With this setup, you won't need to manage server infrastructure — everything will be updated automatically.

---

## Hardware Components

- **Raspberry Pi 3 Model B** (Wi-Fi preferred, since it may be deployed outdoors)
- **RTL-SDR V3** (software-defined radio dongle)
- **Dipole Antenna** (tuned to 137 MHz)
- **Coaxial Cable** (to connect the antenna to the Pi)

## Software & Services

- **AWS S3** (for image hosting)
- **Node.js** (for scripting)
- **Predict** (to forecast satellite passes)
- **RTL-SDR drivers** (to interact with the radio dongle)
- **NOAA APT** (for weather satellite decoding)
- **Cron Jobs** (for automating tasks)

---

## Steps

1. **Set up Raspberry Pi**:
   - Install Raspbian OS on the Pi.
   - Set up Wi-Fi connectivity (optional if using Ethernet).
   
2. **Install RTL-SDR**:
   - Install the necessary RTL-SDR libraries and drivers.
   - Configure the SDR for 137 MHz weather satellite signals.

3. **Set up Antenna**:
   - Build or buy a dipole antenna tuned to 137 MHz.
   - Connect the antenna to the RTL-SDR using coaxial cable.

4. **Install Weather Satellite Decoding Software**:
   - Install `noaa-apt` or `wxtoimg` for satellite image decoding.

5. **Automate Satellite Pass Prediction**:
   - Use `predict` to forecast satellite passes over your location.
   - Schedule automatic capturing and decoding using `cron` jobs.

6. **Upload Images to AWS S3**:
   - Set up an S3 bucket on AWS.
   - Write a Node.js script to upload the decoded images to S3.

7. **Automate the Entire Workflow**:
   - Use `cron` to automate the entire process from receiving, decoding, and uploading the images.

---

## Useful Resources

- [Raspberry Pi Documentation](https://www.raspberrypi.org/documentation/)
- [RTL-SDR Setup Guide](https://www.rtl-sdr.com/rtl-sdr-quick-start-guide/)
- [AWS S3 Documentation](https://aws.amazon.com/s3/)
