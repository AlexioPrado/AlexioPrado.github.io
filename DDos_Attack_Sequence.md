## Distributed Denial of Service Attack

```mermaid
sequenceDiagram
participant Attacker
participant BotNet
participant WebServer
participant Firewall

Attacker ->>+ BotNet: Go bots, attack the web!
BotNet ->>+ WebServer: Lets go to the server and wreak havoc!
Attacker ->>+ BotNet: Go.... NOW!
BotNet ->>+ WebServer: Bot 1: GO!
BotNet ->>+ WebServer: Bot 2: Havoc!
BotNet ->>+ WebServer: Bot 3: WOOHOO!
BotNet ->>+ WebServer: Bot 4: GO GO!
BotNet ->>+ WebServer: Bot 5: Traffic!
WebServer ->>+ Firewall: Ahhh, the agony! Help!
Firewall -->> WebServer: Detecting source of connections...
WebServer ->>+ BotNet: Block! No more acceptiong connection from this source!
BotNet -->> WebServer: Oh No! What happend?

```
### Documentation
Steps into a DDos Attack!<br>
1. Attacker sends instructions and commands to the BotNet
2. BotNet, with the command of the Attacker will connect to the WebServer and cause traffic
3. WebServer, oerwhelmed by the ammount of traffic can't respond to real connections by users
4. The firewall however can stop connections from specific sources.
5. Firewall closes connection from the BotNet, stopping the Attack
