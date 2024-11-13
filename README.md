# PlanEth Hackathon

    A planet consists of Mandalases in the EVM universe.

## Guidline

### Overview

This guide outlines the architecture for building a Web3 ecosystem that enables multiple communities to operate with their own currencies while allowing inter-community token swaps. The ecosystem supports businesses, users, and community governance.

[![](https://mermaid.ink/img/pako:eNqNVU2P0zAQ_StRTiC2q91rDkh8CwlE1cIF9TJNpllrYzuM7UK06n9nnKTZ2PmAXNK85xm_Nx2Pn9JcF5hmaV6BMe8FlATyoBJ-WiT5kGvTGItyh6UwlprkqaP984paEOmdltIpYZsXL0esU-t8iXYgPquTDkhhdn0wFgvp6wIsLmbY5D0j0CQS6lqosmMvBzW2OGT4CLnVkcOccLxJIKDAutLNwH3Xj6iCBQatqwf-kz4jKVA5BjK7LM8mvVwggmZdbLtbIFUKZYPtj45CPZZAmRNSAHJliJWFC7WFau_qugodH6Hy-r-dAgcKJI4-TSOPugoc5kJCZdYNPZcncMXiam1CeWdtQwD_YO4irMAKSwjBTZeNtYQd0XKclYEtktDFrNS25PvfUC83ime3ICju8yX8TVV52IQiPbLasoMSHxzIgKL4In45UcTNSii5wPOc4Uyxsh0apDOGyqzf9y4G7kcAdWF3U-h-1slbZ4RCY1bHy3XRwnSZp9vpcKUm44UdLnGbY0_8Y278YFursv2CGU0e3pI-iQpjSZ6ayHEMLimZjufNZjrQMo5WUGJ_Aif87e3reLBkSdfQ_xUyOrpR3OTI-Liwe6OIWUeTLskSQh5kyFuuxQV_0TQm8swBsbT2KEaLR27Hxb7WrWxpk96kEkmCKPh2bbvjkNoH5EmZZvyzAHo8pAd14XXgrN43Kk8zSw5v0q5N-sv4CpJ25UOanXh28VcN6qfWcvhGPtOavvZ3uX9d_gIVo3wd?type=png)](https://mermaid.live/edit#pako:eNqNVU2P0zAQ_StRTiC2q91rDkh8CwlE1cIF9TJNpllrYzuM7UK06n9nnKTZ2PmAXNK85xm_Nx2Pn9JcF5hmaV6BMe8FlATyoBJ-WiT5kGvTGItyh6UwlprkqaP984paEOmdltIpYZsXL0esU-t8iXYgPquTDkhhdn0wFgvp6wIsLmbY5D0j0CQS6lqosmMvBzW2OGT4CLnVkcOccLxJIKDAutLNwH3Xj6iCBQatqwf-kz4jKVA5BjK7LM8mvVwggmZdbLtbIFUKZYPtj45CPZZAmRNSAHJliJWFC7WFau_qugodH6Hy-r-dAgcKJI4-TSOPugoc5kJCZdYNPZcncMXiam1CeWdtQwD_YO4irMAKSwjBTZeNtYQd0XKclYEtktDFrNS25PvfUC83ime3ICju8yX8TVV52IQiPbLasoMSHxzIgKL4In45UcTNSii5wPOc4Uyxsh0apDOGyqzf9y4G7kcAdWF3U-h-1slbZ4RCY1bHy3XRwnSZp9vpcKUm44UdLnGbY0_8Y278YFursv2CGU0e3pI-iQpjSZ6ayHEMLimZjufNZjrQMo5WUGJ_Aif87e3reLBkSdfQ_xUyOrpR3OTI-Liwe6OIWUeTLskSQh5kyFuuxQV_0TQm8swBsbT2KEaLR27Hxb7WrWxpk96kEkmCKPh2bbvjkNoH5EmZZvyzAHo8pAd14XXgrN43Kk8zSw5v0q5N-sv4CpJ25UOanXh28VcN6qfWcvhGPtOavvZ3uX9d_gIVo3wd)

[![](https://mermaid.ink/img/pako:eNqlVdFumzAU_RXLVaVNgilapD4gbVJotr1s0rR0Lxt7cOA6WDE2sk0z1PbfZ-PgAC1a2voJH5977uHei7nDuSwAJ5hyechLogy6WWcC2XV5idZAmQCkTctBowMzJdqCMaBQLoVRRBtP5UzsN46ECqCk4caGKLmH-MAKUybv679RLrlUycVyufQhnSa6lgoQZZwnF5TCFaWRD-yI0ZzIYrEYivyAHbNUZi16Kbh6qdS1rKpGMNOugpTz9Sqp9NVSmwOpvxOmdCgVLZ6jFPrZlVtDbpg8gg75_SbD3cmm1QYqf_DhtDzwKZe6Oz-Wu-0Fjq_5meRG9uiNNSOc7R7Fb_8MfAw6NnJzwp2nPhH6SlpQM7bSRtsR1Xrs6qcGFZBx7mAYraal6HvvCxJoM5kDo3vZnhbQL_IWlCAiB3s0ZyGdsZCOLaTnWUjnLaQTC643yM_UyEEYNWfAqzpIzxgIfXYxaBVP0xwvEAWcuBy6ZPX4Hrllmm3tiHOyBa5PM4ni-CO6z3BFBNmBzvD9YDge0wqouWw72qmN59HSx7RcATE-aajHdEBR_M6TFVBQYGv8ZPbzA6bNW4WAumuTq9oTjgbXzH_4OMIVqIqwwl73dy46w6aECjKc2MeCqH2GM_FgeaQxctOKHCdGNRDhpi5sQdaM7BSpelDJZlfihBKu7a4m4peUVdhDweyH_83_XLp_zMM_eiEfeg?type=png)](https://mermaid.live/edit#pako:eNqlVdFumzAU_RXLVaVNgilapD4gbVJotr1s0rR0Lxt7cOA6WDE2sk0z1PbfZ-PgAC1a2voJH5977uHei7nDuSwAJ5hyechLogy6WWcC2XV5idZAmQCkTctBowMzJdqCMaBQLoVRRBtP5UzsN46ECqCk4caGKLmH-MAKUybv679RLrlUycVyufQhnSa6lgoQZZwnF5TCFaWRD-yI0ZzIYrEYivyAHbNUZi16Kbh6qdS1rKpGMNOugpTz9Sqp9NVSmwOpvxOmdCgVLZ6jFPrZlVtDbpg8gg75_SbD3cmm1QYqf_DhtDzwKZe6Oz-Wu-0Fjq_5meRG9uiNNSOc7R7Fb_8MfAw6NnJzwp2nPhH6SlpQM7bSRtsR1Xrs6qcGFZBx7mAYraal6HvvCxJoM5kDo3vZnhbQL_IWlCAiB3s0ZyGdsZCOLaTnWUjnLaQTC643yM_UyEEYNWfAqzpIzxgIfXYxaBVP0xwvEAWcuBy6ZPX4Hrllmm3tiHOyBa5PM4ni-CO6z3BFBNmBzvD9YDge0wqouWw72qmN59HSx7RcATE-aajHdEBR_M6TFVBQYGv8ZPbzA6bNW4WAumuTq9oTjgbXzH_4OMIVqIqwwl73dy46w6aECjKc2MeCqH2GM_FgeaQxctOKHCdGNRDhpi5sQdaM7BSpelDJZlfihBKu7a4m4peUVdhDweyH_83_XLp_zMM_eiEfeg)

### System Components

#### Core Components

1. **Communities**: Self-contained units with their own currency and governance
2. **Businesses**: Service providers within communities
3. **Users**: Community members who can hold tokens and participate in activities
4. **Token Swaps**: Mechanism for exchanging tokens between communities

### Smart Contract Architecture

#### Core Contracts

1. **EcosystemRegistry**

   - Central registry for all communities
   - Manages community registration/unregistration
   - Single source of truth for community information

   ```solidity
   // Key functions
   function registerCommunity()
   function unregisterCommunity()
   function getCommunityInfo()
   function isRegisteredCommunity()
   ```

2. **CommunityFactory**
   - Deploys new communities
   - Creates community tokens
   - Sets up governance structures
   ```solidity
   // Key functions
   function createCommunity()
   function deployCommunityToken()
   function setupCommunityGovernance()
   ```

#### Community-Specific Contracts

1. **CommunityToken**

   - ERC20 token implementation
   - Community-specific currency

   ```solidity
   // Key functions
   function mint()
   function burn()
   function transfer()
   function approve()
   ```

2. **CommunityGovernance**
   - Handles community decision-making
   - Manages proposals and voting
   ```solidity
   // Key functions
   function propose()
   function vote()
   function execute()
   function delegate()
   ```

#### Token Swap Contracts

1. **TokenSwapFactory**

   - Creates and manages swap pairs
   - Maintains pair registry

   ```solidity
   // Key functions
   function createSwapPair()
   function getSwapPair()
   function getAllPairs()
   ```

2. **TokenSwapPair**
   - Handles token swaps between communities
   - Manages liquidity pools
   ```solidity
   // Key functions
   function addLiquidity()
   function removeLiquidity()
   function swap()
   function getReserves()
   ```

#### Registry Contracts

1. **BusinessRegistry**

   - Manages business registrations
   - Stores business metadata

   ```solidity
   // Key functions
   function registerBusiness()
   function unregisterBusiness()
   function updateBusinessInfo()
   ```

2. **UserRegistry**
   - Manages user profiles
   - Handles permissions
   ```solidity
   // Key functions
   function registerUser()
   function updateUserProfile()
   function getUserInfo()
   ```

### Deployment Flow

1. Deploy Core Contracts:

   - EcosystemRegistry
   - CommunityFactory
   - TokenSwapFactory

2. Deploy Registry Contracts:

   - BusinessRegistry
   - UserRegistry

3. For Each Community:

   - Deploy CommunityToken
   - Deploy CommunityGovernance
   - Register in EcosystemRegistry

4. For Token Swaps:
   - Deploy TokenSwapPair for each community pair
   - Initialize liquidity pools

### Key Features

1. **Community Management**

   - Independent governance
   - Custom token economics
   - Business integration

2. **Token Swaps**

   - Cross-community trading
   - Automated market making
   - Liquidity provision

3. **Business Integration**

   - Registration system
   - Multi-token support
   - Service marketplace

4. **User Features**
   - Multi-community membership
   - Token swapping
   - Governance participation

### Development Guidelines

1. **Smart Contract Best Practices**

   - Use OpenZeppelin contracts where possible
   - Implement comprehensive testing
   - Follow security best practices

2. **Security Considerations**
   - Implement access controls
   - Rate limiting for sensitive operations
   - Reentrancy protection
   - Integer overflow protection

### Hackathon Track Suggestions

1. **Community Builder Track**

   - Implement community creation and management
   - Build governance mechanisms
   - Design token economics

2. **DeFi Track**

   - Implement token swap mechanisms
   - Build liquidity provision systems
   - Create yield farming opportunities

3. **Business Integration Track**

   - Build business onboarding system
   - Create service marketplace
   - Implement payment systems

4. **User Experience Track**
   - Design user interfaces
   - Build wallet integration
   - Create community interaction tools

### Resources

1. **Technical Stack**

   - Solidity
   - Hardhat/Truffle
   - OpenZeppelin
   - Ethers.js

2. **Testing Tools**

   - Hardhat
   - Ethers.js

3. **Frontend Frameworks**
   - React
   - Tailwind
   - Ether JS
