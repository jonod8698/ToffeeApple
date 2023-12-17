Open files and links in a temporary macOS VM.

## Requirements
### Host System
- macOS arm64 / Apple Silicon
- [Tart](https://github.com/cirruslabs/tart)

## Quick Start
1. Clone this repo and install Tart
```zsh
git clone https://github.com/jonod8698/ToffeeApple.git
cd ToffeeApple
brew install cirruslabs/cli/tart
```

2. Download a pre-built Base VM from cirruslabs. Note: To build your own Base VM see [Base VM Customization](#base-vm-customization).
```zsh
tart clone ghcr.io/cirruslabs/macos-sonoma-base:latest sonoma-base
```

3. Start the VM and configure `softnet` for network isolation.
```zsh
tart run sonoma-base --net-softnet
```

3. Close the VM then run `prepare.sh`. Enter the password for the VM when prompted.
```zsh
./prepare.sh
```

4. Start the VM


5. Close the VM by typing exit (or Control + C). By default, the temporary VM will be deleted. To keep the VM, add `-d false`.

## Usage

```zsh
./vm_utility_script.sh [-u URL] [-f file path] [-t time limit] [-o OS version] [-h help]
```

### Options
- u: URL to open in the VM.
- f: File to run in the VM.
- t: VM duration, default no time limit.
- o: Specify the OS version, default is Ventura.
- h: Display usage information.


## Base VM Customization
Refer to [macOS Sandbox VM](https://github.com/jonod8698/macos-sandbox-vm#base-vm-customization).