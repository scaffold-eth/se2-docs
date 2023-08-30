---
sidebar_position: 1
---

# Address

Display an address (or ENS) plus a copy address icon utility. If the address has an ENS associated with avatar, it will show its avatar, if not it will show a blockie image for that address.

By default, clicking on the address sends you to blockexplorer details for that address.

![Address Example](/img/Address.png)

## Import

```ts
import { Address } from "~~/components/scaffold-eth";
```

## Usage

```ts
const [selectedAddress, setSelectedAddress] = useState("");

<Address address={selectedAddress} />;
```

## Props

- `address` => Pass the address in `0x___` format, it will resolve ENS if it's associated.

- `disableAddressLink` => Set it to `true` to disable the blockexplorer link behaviour when clicking on the address.

- `format` => By default displayed address it's only the first five characters from the address, set this to `"long"` to display the full address.