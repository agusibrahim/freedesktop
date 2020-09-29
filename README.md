# #freedesktop
> Get your remote desktop for free

Need to test your desktop application? This is a free remote desktop from Github.
I'm using Macbook, sometimes I need Windows to run certain applications. Thanks Github, I no longer need VM or Bootcamp which is quite draining my hard drive
Windows             |  Linux (Ubuntu)
:------------------:|:-------------------------:
![](https://i.imgur.com/LjjPu62.png)  |  ![](https://i.imgur.com/6kt0ad4.png)

## How it's Work?
It's using [Github Action](https://github.com/features/actions), the awesome CI/CD feature from Github. Combined with [Ngrok](https://ngrok.com) so that it can be accessed by public. Basically it just Enable RDP on Windows/Linux and install GUI on Linux then reverse connection with Ngrok.

## Getting started
First, [Click here](https://github.com/agusibrahim/freedesktop/generate) or click the green button "Use this template" to clone this template to your repository, rename whatever you want.
Make sure this repo is yours. 
Login to your Ngrok account or [Sign up here](https://dashboard.ngrok.com/signup). Goto [Setup page](https://dashboard.ngrok.com/get-started/setup) and copy your random Auth token something like `1hdFJgQC6ihak1ESbpx1t1R4356_2JLmorDVGYbBixWv7Xftm`

Edit file `/.github/workflows/linux.yaml` or `/.github/workflows/windows.yaml` and replace `YOUR-NGROK-TOKEN-HERE` with your Ngrok authtoken, you can also change Desktop password here.
Last step, run the github workflow as shown below

![Tutorial](https://raw.githubusercontent.com/agusibrahim/freedesktop/master/freedesktop-demo.gif)

## Stop the Desktop
Your desktop can run for up to 6 hours, if your work is done you can stop it. To stop the session, click red button "Cancel workflow". Shutting down the desktop *Won't stop* the workflow runner.

## Limitation
- You'll able to use this desktop max 6 hour, starting since you're clicking "Run workflow". Make sure your repo set to public otherwise you have strict monthly limit.

## Notes
- Don't store important files here because files will be permanently deleted when the runner stop.
- For Windows, don't close this guy or your connection will interrupted
<img src="https://i.imgur.com/lhztr7E.png" width="250"/>

- All files in this repo will appear in runner directory. If there is a new file that you want to appear to the internet, just put your file to the `artifact` folder and file will upload as Workflow artifact.
- In Linux you'll able connect via SSH. Just see workflow logs for login detail

