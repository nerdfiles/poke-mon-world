# Pokémon World

People as Pokémon.

## Overview

Turns mobile device into an Augmented Reality (AR) Game where users choose to 
be Pokémon (Customers) or Pokémasters (Merchants). When “captured” Pokémon 
Users may access secret commercial tunnels for a kind of telepathic 
underground economy of Pokégovernance. Co-habitate “Sims”-esque 
styled modular zones that each Pokémaster prepares. Naturally, the 
limit of “walking chatrooms” is up to the charisma and tenacity of 
the Pokémaster. Pokémasters at the same time enjoy the abilities 
to call upon virtualized embodiments of their Pokémon Users, for costs of 
their HP in reward for currency. The Pokémasters, in similar fashion, 
wage their battles for the viability of reward (currency), treasure, 
experience, and evolution of their Pokémon Users (if such a user gambles 
her HP, she gets the risk of evolution, and percentage of group reward).

## Asset Management

### Aliases

Toward a more REST-ful interface, we set up the following Aliases:

    aka
      has-surf # P2PKH Base Subaccounts or Pokémasters Accounts
        [DATA] goto
        [DATA] acl
    aka
      can-evolve # Pokémon Accounts
        [DATA] goto
        [DATA] acl

A more complete example for closed systems:

```
    aka
      can-view # Pokémasters Accounts
        [DATA] goto
          /asset/p2pkh/Xj8nk3.../
        [DATA] acl
          [
              {
                  "subjects": [ { "addresses": [ ], "required": 0 } ],
                  "permissions": { "account_modify": "Permit", "account_create": "Permit" }
              },
              {
                  "subjects": [ { "addresses": [ "<some-other-address>" ], "required": 1 } ],
                  "permissions": { "account_spend": "Permit" }
              }
          ]
```

### Assets

    asset
      Pokéball
        [ACC] /asset/Pokéball/
        [DATA] asdef

### Actions

    asset
      p2pkh
        {{Xj8nk3...}}
          [ACC] /asset/p2pkh/Xj8nk3...
          [DATA] asdef

### Normal Users

Where to receive funds:

    p2pkh
      <address>
        [ACC] /asset/p2pkh/Xj8nk3...
      MusicRecording
        [ACC] /asset/Pokéball/

### Subaccounts

    /account/KanyeWest/:DATA:goto
