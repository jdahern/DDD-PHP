# DDD-PHP
A folder description for DDD and PHP

## Folder Structure

```

.
+-- Clients/                                        # Everything in Clients should be slim, and really call a service, and return the response
|   +-- HTTP/                                       # May have limited static files.
|   |   +-- { First Part }/
|   |   |   +-- { Controller Name }.php             # Controllers are narrow scope and still should have a C.R.A.P. < 30
|   |   |   +-- { Some JS }.{js|coffee|ts}
|   |   |   +-- { Some CSS }.{css|less}
|   |   |   +-- { Some template }.{tpl|mt|volt}
|   |   |   |
|   |   |   +-- { Second Part }/                    # Nesting for the HTTP is Inf deep
|   |   |   |   +-- { Controller Name }.php
|   |   |
|   |   +-- Commons/                                # Used for site wide or commonly used scripts
|   |   |   +-- { Commons Name } /                  # Each should be its own world (use NPM / Bower)
|   |   |   |   +-- { Some JS }.{js|coffee|ts}
|   |   |   |   +-- { Some CSS }.{css|less}
|   |   |   |   +-- { Some template }.{tpl|mt|volt}
|   |
|   +-- CLI/                                        # A map from { Main Group Name }:{Command Name}Command.php for each command
|   |   +-- { Main Group Name }/                    # Following Symphony CLI syntax, only this deep for CLI
|   |   |   +-- {Command Name}Command.php           # The command
|   |
|   +-- API/                                        # Should have caching built in for REST like
|   |   +-- {Aggregate Root}/
|   |   |   +-- {Action}.php
|
+-- Domain/                                         # Each root should be its own world (use composer)
|   +-- {Domain Aggregate Root}/
|   |   +-- Configuration/
|   |   +-- Contracts/                              # ?? Maybe at base level ??
|   |   +-- Repositories/
|   |   +-- Entities/
|   |   +-- Notifications/
|   |   +-- EventHandlers/
|   |   +-- Events/
|   |   +-- CommandHandlers/
|   |   +-- Commands/
|   |   +-- Entities/
|   |   +-- Services/
|   |   +-- {Action}.php
|   |   +-- composer.json
|   |   +-- README.md
|   |   +-- gulpfile.js
|   |   +-- {other require files}.{ext}
|
+-- Service/
|   +-- Cart/
|   |   +-- CartToOrder.php
|   +-- Shipping/
|   |   +-- Methods/
|   |   +-- ShippingCalculator.php
|
+-- Infrastructure/
|   +-- Notifications/
|   +-- Logging/
|   +-- CLI/
|   +-- Cache/
|   +-- Configuration/
|   +-- DI/
|   +-- Emails/
|   +-- WebServer/

```

