---
sidebar_position: 1
---

# Address

Display an address (or ENS) along with a utility icon to copy the address. If the address is associated with an ENS that has an avatar, this avatar will be displayed. If not, a blockie image representation of the address will be shown.

By default, clicking on the address redirects you to the `targetNetwork` blockexplorer with the details of that address.

![Address Example](/img/Address.png)

## Import

```tsx
import { Address } from "~~/components/scaffold-eth";
```

## Usage

```tsx
<Address address="0x34aA3F359A9D614239015126635CE7732c18fDF3" />
```

## Props

- `address` => Address in `0x___` format, it will resolve its ENS if has one associated.

- `disableAddressLink` => Set it to `true` to disable the blockexplorer link behaviour when clicking on the address.

- `format` => By default, only the first five characters of the address are displayed. Set this to `"long"` to display the entire address.

- `size` (optional) => Size for the displayed Address component. `base` by default but you can pass in `xs`, `sm`, `base`, `lg`, `xl`, `2xl`, `3xl`.