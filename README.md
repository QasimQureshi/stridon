## Introducing Stridon
Stridon brings together journalists who want to publish articles and readers who want to read them. Think _decentralized Medium._
## Purpose
- Be a proof of concept for a new journalism model made possible by NuCypher's _unconditional privacy_
- Serve as an example of how Django can be used to build with NuCypher
## System Overview
Alison is a journalist and likes Stridon's vision for a more equitable journalism model so she joins Stridon’s news service. Stridon can distribute news articles that Alison publishes in encrypted form. Alison wants her news articles to reach users (readers) of Stridon… by joining the Stridon service Alison has created a policy public key (thanks to NuCypher!) so Stridon users (readers) can have access to her encrypted news articles.

Stridon uses this policy public key to encrypt the news article data that Alison publishes. Article data is saved to Stridon’s Django database.

Alison wants her articles distributed to the users of Stridon. Stridon manages the users (readers) public keys and creates a policy (within the NuCypher network) on Alison’s behalf which grants users access to her articles. Stridon users can read the encrypted news articles by using their private keys to request a re-encrypted ciphertext for each news article.

Stridon has been designed to enable the same monetisation as Medium. So Alison can chose to allow her article to be available to the entire Stridon user base or only to those who have signed up for a paid membership.
## Current Design
NuCypher love Python. For that reason we've used the ever popular Django framework to bring the power of NuCypher to a web app.

This proof of concept intends to demonstrate that Alison can have confidence that neither Stridon or any 3rd party can alter her articles, and that if she wished she could control her own keys but has the option to trust Stridon.

Within NuCypher we have two policies. Paid and Free. When joining Stridon all users will be placed in the Free policy. When a user becomes a Paid member they will be given access to the additional Paid policy.
# Installing the demo
### STEP 1 - Clone the project
Clone the project to your project area

C:\PythonProjects>git clone https://github.com/SagarKishore-PFM/Stridon-Test.git

C:\PythonProjectst> cd Stridon-Test

### STEP 2 - Build and Run the Application
Open an Anaconda Prompt and go to a virtual environment where you have NuCypher and Django available.

(screenshots to follow)

## Limitations
Due to time limitations certain comprimises have been made, for example we are yet to add user friendly features such as the ability to edit news articles.
## Future Development
We'd like to split the system into separate applications. For example Desktop Apps for writing / publishing and Mobile Apps for reading.
