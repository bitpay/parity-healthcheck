# Goal
Use web3 to detect when parity should be restarted

Optionally add other healthchecks

## Config

```
module.exports = {
  restartOnIssue: true,
  host: 'localhost',
  httpPort: 8545,
  wsPort: 9546,
  wsProtocol: "ws",
  detect: {
    notSyncing: true,
    websocketsStuck: true,
    slowApi: true
  }
};
```

# Setup
* Clone repo
* `npm install`
* ./register-service
* sudo vim /etc/systemd/system/parity-healthcheck.service
* set ExecStart path for parity-healthcheck/index.js 
