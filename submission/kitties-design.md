A pallet for collecting kitties.

- traits
    - Types
        - struct Kitty
            - kitty_id: u64
            - dna: u128
            - owner_id: AccountId (cannot be null)
- Storage
    - Kitties: map AccountId => Vec
- Calls
    - fn create_kitty
- Events
    - KittyCreated
        - kitty_id: KittyId
        - owner_id: AccountId
- Module
    - fn create_kitty
        - creates a 128 bit DNA with [Random Seed](https://substrate.dev/recipes/randomness.html)
        - assigns the AccountId caller as Owner
