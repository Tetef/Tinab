# Tinab
This Is Not Another Blockchain.

The ultimate goal here is implement a crypto-currency based on a peer to peer consensus protocol wich doesn't require any cryptographic proof such as a proof of work or a proof of stake. Here messages suffice to reach consensus on a the ledger.

The project thus holds 2 parts :
 - The consensus protocol
 - The cryptocurrency based on the consensus protocol

The consensus protocol is a simplified version of David Mazières' "Stellar Consensus Protocol". Here is how it works :

For a statement s to be ratfied, a node v sends a vote message with its quorum slices Q(v) wich are a set of sets of peer nodes.

A quorum is set B of nodes containing at least one quorum slice of each of its members.
B is a quorum <=> For all v in B, there exists Q in Q(v) such that q is included in B.

A statement is accepted when a quorum is reached around it.

Nodes accepting the statement send a message stating their state "accept s"
