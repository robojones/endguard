# Endguard API

## Handshake

### CreateConnectionOffer

### ApplyConnectionOffer

### ApplyConnectionConfirmation

## Secure Channel

### Encrypt

#### Parameters

- **plaintext** `List<byte>` Data to encrypt
- **aad** `List<byte>` Associated Authenticated Data is not encrypted but only authenticated.
  The aad can be sent as plaintext along with the ciphertext of the message and is authenticated during the decryption.

#### Returns

- **ciphertext** `List<byte>`
- **nonce** `List<byte>`
- **mac** `List<byte>`

### Decrypt

#### Parameters

- **ciphertext** `List<byte>`
- **nonce** `List<byte>`
- **mac** `List<byte>`
- **aad** `List<byte>` Associated Authenticated Data is not encrypted but only authenticated.
  The aad can be sent as plaintext along with the ciphertext of the message and is authenticated during the decryption.

#### Returns

- **plaintext** `List<byte>`
