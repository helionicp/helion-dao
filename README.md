# `Helion AI Dao`


## Description

This is a full implementation of the ICRC-1 fungible token standard for the Helion AI DAO.

## Getting Started 

- Replace the values enclosed in `< >` with your desired values and run in the terminal

```motoko
    git clone https://github.com/helionicp/helion-dao
    cd helion-dao
    mops install
    dfx start --background --clean

    dfx deploy helion-dao-backend --argument '( record {                     
        name = "<Insert Token Name>";                         
        symbol = "<Insert Symbol>";                           
        decimals = 6;                                           
        fee = 1_000_000;                                        
        logo = "data:image/png;base64,iVBORw0...K5CYII=";                                        
        max_supply = 1_000_000_000_000;                         
        initial_balances = vec {                                
            record {                                            
                record {                                        
                    owner = principal "<Insert Principal>";   
                    subaccount = null;                          
                };                                              
                100_000_000                                 
            }                                                   
        };                                                      
        min_burn_amount = 10_000;                         
        minting_account = null;                                 
        advanced_settings = null;                               
    })'
  ```
