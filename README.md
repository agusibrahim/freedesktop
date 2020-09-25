# #freedesktop
> Get your remote desktop for free

Need to test your desktop application? This is a free remote desktop from Github.
I'm using Macbook, sometimes I need Windows to run certain applications. Thanks Github, I no longer need VM or Bootcamp which is quite draining my hard drive

## How it's Work?
It's using [Github Action](https://github.com/features/actions), the awesome CI/CD feature from Github. Combined with [Ngrok](https://ngrok.com) so that it can be accessed by public. Basically it just Enable RDP on Windows/Linux and install GUI on Linux then reverse connection with Ngrok.

## Get started
First, [Click here](https://github.com/agusibrahim/freedesktop/generate) or click the green button "Use this template" to clone this template to your repository, rename whatever you want.
Make sure this repo is yours. 
Login to your Ngrok account or [Sign up here](https://dashboard.ngrok.com/signup). Goto [Setup page](https://dashboard.ngrok.com/get-started/setup) and copy your random Auth token something like `1hdFJgQC6ihak1ESbpx1t1R4356_2JLmorDVGYbBixWv7Xftm`

Edit file `/.github/workflows/linux.yaml` or `/.github/workflows/windows.yaml` and replace `YOUR-NGROK-TOKEN-HERE` with your Ngrok authtoken, you can also change Desktop password here.
Last step, run the github workflow as shown below

![Tutorial](https://raw.githubusercontent.com/agusibrahim/freedesktop/master/freedesktop-demo.gif)

