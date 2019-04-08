# Stridon
Stridon brings together journalists who want to publish articles and readers who want to read them. _Think decentralized Medium.
# System Overview
Alison is a journalist and likes Stridon's vision for a more equitable journalism model so she joins Stridon’s news service. Stridon can distribute news articles that Alison publishes in encrypted form. Alison wants her news articles to reach users (readers) of Stridon… by joining the Stridon service Alison has created a policy public key (thanks to NuCypher!) so Stridon users (readers) can have access to her encrypted news articles.

Stridon uses this policy public key to encrypt the news article data that Alison publishes. Article data is saved to Stridon’s Django database.

Alison wants her articles distributed to the users of Stridon. Stridon manages the users (readers) public keys and creates a policy (within the NuCypher network) on Alison’s behalf which grants users access to her articles. Stridon users can read the encrypted news articles by using their private keys to request a re-encrypted ciphertext for each news article.

Stridon has been designed to enable the same monetisation as Medium. So Alison can chose to allow her article to be available to all of the Stridon user base or only to those who have signed up for a paid membership.
# Current Design
Within NuCypher we have two policies. Paid and Free. When joining Stridon all users will be placed in the Free policy. When a user becomes a Paid member they will be given access to the additional Paid policy.
