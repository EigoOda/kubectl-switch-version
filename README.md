
# kubectl version switch

## What is kubectl version switch

* Switch kubectl version plugin.
  * Make sure the client and server version are the same.
  * Closely related to asdf.

## Dependencies

* asdf
  * [How to install asdf]


### Examples

```
$ kubectl version
Client Version: version.Info{Major:"1", Minor:"19", GitVersio:"v1.19.0", GitCommit:"e19964183377d0ec2052d1f1fa930c4d7575bd50", GitTreeState:"clean", BuildDate:"2020-08-26T14:30:33Z", GoVersion:"go1.15", Compiler:"gc", Platform:"darwin/amd64"}
Server Version: version.Info{Major:"1", Minor:"21", GitVersion:"v1.21.7", GitCommit:"1f86634ff08f37e54e8bfcd86bc90b61c98f84d4", GitTreeState:"clean", BuildDate:"2021-11-18T00:11:23Z", GoVersion:"go1.16.10", Compiler:"gc", Platform:"linux/amd64"}

$ kubectl switch-version
Switch to version: 1.21.8

$ kubectl version
Client Version: version.Info{Major:"1", Minor:"21", GitVersion:"v1.21.8", GitCommit:"4a3b558c52eb6995b3c5c1db5e54111bd0645a64", GitTreeState:"clean", BuildDate:"2021-12-15T14:52:11Z", GoVersion:"go1.16.12", Compiler:"gc", Platform:"darwin/amd64"}
Server Version: version.Info{Major:"1", Minor:"21", GitVersion:"v1.21.7", GitCommit:"1f86634ff08f37e54e8bfcd86bc90b61c98f84d4", GitTreeState:"clean", BuildDate:"2021-11-18T00:11:23Z", GoVersion:"go1.16.10", Compiler:"gc", Platform:"linux/amd64"}

$ asdf global kubectl 1.19.0

$ asdf uninstall kubectl 1.21.8

$ kubectl version
Client Version: version.Info{Major:"1", Minor:"19", GitVersion:"v1.19.0", GitCommit:"e19964183377d0ec2052d1f1fa930c4d7575bd50", GitTreeState:"clean", BuildDate:"2020-08-26T14:30:33Z", GoVersion:"go1.15", Compiler:"gc", Platform:"darwin/amd64"}
Server Version: version.Info{Major:"1", Minor:"21", GitVersion:"v1.21.7", GitCommit:"1f86634ff08f37e54e8bfcd86bc90b61c98f84d4", GitTreeState:"clean", BuildDate:"2021-11-18T00:11:23Z", GoVersion:"go1.16.10", Compiler:"gc", Platform:"linux/amd64"}

$ kubectl switch-version
Same kubectl version missing as server's.
Installing target version .....
1.21.8 installed !!
Switch to version: 1.21.8

$ kubectl version
Client Version: version.Info{Major:"1", Minor:"21", GitVersion:"v1.21.8", GitCommit:"4a3b558c52eb6995b3c5c1db5e54111bd0645a64", GitTreeState:"clean", BuildDate:"2021-12-15T14:52:11Z", GoVersion:"go1.16.12", Compiler:"gc", Platform:"darwin/amd64"}
Server Version: version.Info{Major:"1", Minor:"21", GitVersion:"v1.21.7", GitCommit:"1f86634ff08f37e54e8bfcd86bc90b61c98f84d4", GitTreeState:"clean", BuildDate:"2021-11-18T00:11:23Z", GoVersion:"go1.16.10", Compiler:"gc", Platform:"linux/amd64"}n

```

### Installation

```
$ git clone https://github.com/dubs11kt/kubectl-version-switch.github

$ cd kubectl-switch-version
$ chmod +x kubectl-switch-version
$ mv kubectl-switch-version /usr/local/bin
```


[How to install asdf]: https://asdf-vm.com/guide/getting-started.html
