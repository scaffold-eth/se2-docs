---
sidebar_position: 1
title: Simplified Get balance of the connected account
description: Learn how to retrieve and display the ETH balance of the connected account in your dApp.
---

# Get the Current Balance of the Connected Account

This recipe shows how to fetch and display the ETH balance of the currently connected account in your decentralized application.

```tsx
import { useAccount } from "wagmi";
import { Address, Balance } from "~~/components/scaffold-eth";

export const ConnectedAddressBalance = () => {
  const { address: connectedAddress } = useAccount();

  return (
    <div className="bg-base-300 p-6 rounded-lg max-w-md mx-auto mt-6">
      <h2 className="text-lg font-bold mb-2">Your Ethereum Balance</h2>

      <div className="text-sm font-semibold mb-2">
        Address: <Address address={connectedAddress} />
      </div>

      <div className="text-sm font-semibold">
        Balance: <Balance address={connectedAddress} />
      </div>
    </div>
  );
};
```

## Implementation guide

### Step 1: Create a new Component

Begin by creating a new component in the "components" folder of your application. We will name it "ConnectedAddressBalance.tsx".

```tsx
import { useAccount } from "wagmi";
import { Address, Balance } from "~~/components/scaffold-eth";

export const ConnectedAddressBalance = () => {
  // Your component code will go here.
};
```

### Step 2: Retrieve the Connected Account

Fetch the Ethereum address of the currently connected account using the [useAccount wagmi hook](https://wagmi.sh/react/hooks/useAccount).

```tsx
const { address: connectedAddress } = useAccount();
```

### Step 3: Display the Address and ETH Balance

Now, you can use [Address](/components/Address) and [Balance](/components/Balance) Scaffold ETH-2 components to display the info of your `{connectedAddress}`.

```tsx
return (
  <div className="bg-base-300 p-6 rounded-lg max-w-md mx-auto mt-6">
    <h2 className="text-lg font-bold mb-2">Your Ethereum Balance</h2>

    <div className="text-sm font-semibold mb-2">
      Address: <Address address={connectedAddress} />
    </div>

    <div className="text-sm font-semibold">
      Balance: <Balance address={connectedAddress} />
    </div>
  </div>
);
```