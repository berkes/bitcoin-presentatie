!SLIDE code

 expected_hash = 000012345
 payload = <some data related to things happening on the Bitcoin network>
 nonce = 1

 untill(hash == expected_hash) 
   hash = SHA2( SHA2( payload + nonce ) )
   nonce = nonce + 1

  "Found it!"
