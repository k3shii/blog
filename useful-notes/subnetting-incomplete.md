# Subnetting (incomplete)

## IPV4 Subnetting Calculation

<table><thead><tr><th width="110">Subnet</th><th>/25</th><th>/26</th><th>/27</th><th>/28</th><th>/29</th><th>/30</th><th>/31</th><th>/32</th></tr></thead><tbody><tr><td>Octet</td><td>8</td><td>7</td><td>6</td><td>5</td><td>4</td><td>3</td><td>2</td><td>1</td></tr><tr><td>Subnet Mask</td><td>128</td><td>64</td><td>32</td><td>16</td><td>8</td><td>4</td><td>2</td><td>1</td></tr><tr><td>Host</td><td>256</td><td>128</td><td>64</td><td>32</td><td>16</td><td>8</td><td>4</td><td>2</td></tr></tbody></table>

### Step 1: Classified subnet and usable host

* Default subnet is `/24` which equal to subnet mask of 255.255.255.0

#### Question: The subnet given is /27

To calculate the host, count from behind.

> Think about the octet, /24 needs additional of 3 subnet to make it become subnet of /27, therefore from the octet 8 - 3 and we have the leftover of 5 octet.
>
> So, 2^5 = 32 hosts
>
> To find usable host will always subtract with 2 (subnet id, broadcast id) which represent to the first host and last host within the 32 host range.
>
> Therefore, the usable host equals to 30 host for subnet /27

To calculate the subnet, count from the front.

> As mentioned in previous, we knew that the subnet has borrowed the 3 subnet from the 8 bits.
>
> So, count from the front and sum up all the subnet mask value for the first 3 bits. 128 + 64 + 32.
>
> Therefore, the subnet mask is 224

{% hint style="success" %}
Answer:

Usable host = 30 hosts

Subnet mask = 255.255.255.224
{% endhint %}



Maximum subnet is /32 which equal to subnet mask of 255.255.255.255

To calculate usable host

/27 is given as the subnet and calculate the host by&#x20;

Usable host = Total host - Subnet ID - Broadcast ID

Example:

/24

Subnet mask = 255.255.255.0

Usable host = 254



/25

Subnet mask = 255.255.255.

<table><thead><tr><th width="180">Subnet ID</th><th width="414" align="center">Usable host range</th><th>Broadcast ID</th></tr></thead><tbody><tr><td></td><td align="center"></td><td></td></tr><tr><td></td><td align="center"></td><td></td></tr><tr><td></td><td align="center"></td><td></td></tr><tr><td></td><td align="center"></td><td></td></tr></tbody></table>
