# PFP Registration

### **PFP 프로젝트 등록 화면**&#x20;

PFP 프로젝트 등록 화면 접속 시, 아래와 같은 세가지 메뉴가 뜨게 됩니다.

Link - [http://klu.bs/pfp/add](http://klu.s/pfp/add)

![Klubs PFP Registration Main Page](../.gitbook/assets/17L56Ok2S28Si-HmyqcjWQw.png)

1. [KIP-17 Mintable을 상속한 PFP 등록](https://klu.bs/pfp/add-by-minter)

```
pragma solidity ^0.5.6;

import "./klaytn-contracts/token/KIP17/KIP17Full.sol";
import "./klaytn-contracts/token/KIP17/KIP17Mintable.sol";
import "./klaytn-contracts/token/KIP17/KIP17Burnable.sol";
import "./klaytn-contracts/token/KIP17/KIP17Pausable.sol";

contract DogeSoundClubMate is KIP17Full("DOGESOUNDCLUB MATES", "MATE"), KIP17Mintable, KIP17Burnable, KIP17Pausable {

    string public hash = "6110b42d1575f2bfb80a98cb6ce7d6743fa249b6ee2be08467487c12f5f95753";
    string public ipfs = "QmfTimyAQTQjQsnvECn9U44LdnPzSDF2XREoP2WFdjHitQ";

    function tokenURI(uint256 tokenId) public view returns (string memory) {
        require(_exists(tokenId), "KIP17Metadata: URI query for nonexistent token");
        
        if (tokenId == 0) {
            return "https://api.dogesound.club/mate/0";
```

위와 같이 KIP-17 Mintable를 상속한 PFP 프로젝트의경우 선택하시면 됩니다.
