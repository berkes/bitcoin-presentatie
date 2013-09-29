!SLIDE code

    @@@ ruby
    expected_hash = 000012345
    payload = "The Blockchain" + 
              "The sha-sum of the last block"
              "An extra transaction where I get BTC 25"
    nonce = 1

    untill(hash == expected_hash) {
      hash = SHA2( SHA2( payload + nonce ) )
      nonce = nonce + 1
    }

    print "Found it!"
    announce_to_network(nonce, payload)
