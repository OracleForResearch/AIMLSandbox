## Using the Research Gatway Image

### Overview
The Research gateway image provides a secure gateway to your researech tenancy.Some of the other usages are described below.
1. Secure gateway: Provides a secure gateway with simple deployment. Protects other compute / databases by acting as a gateway.
2. Build: Should be built in a public facing subnet (default)
3. Architecture: One-click compute instance creation on OFR standard architecture
4. OCI-CLI: Comes with pre-installed version of OCI Command line interface (CLI) Tools
5. Configurable: Easily configurable to your tenancy environment
6. Operating system: Currently available as a SSH gatway on Linux operating systems

### Tools and scripts 
1. Following scripts are included with the image
   * OCI-CLI (Command line scripts - installed and pre-configured with a README file)
   * Terminating and startup scripts
   * Block storage attachment and detachment
   * SSH to login to VM in your private subnet
   * Standard Linux monitoring examples
   * Using OCI Telemetry monitoring with OCI-CLI (upcoming)
   * Using NVIDIA monitoring tools with OCI-CLI (upcoming)

### Using the Image
1. Create a compart 
2. Spin up a compute instance using the newly created custom image

### SSH to your private compute instance 

### Guidance and recommendations
1. Build as a free-tier VM with default storage
2. Build in a public subnet
3. Generate a private / public key pair and copy / cut-paste into the VM for secure SSH to your private instances
   * To quickly generate a public / private key pair - try spinning up a compute instance and download the public / private keys.
   * Alternately use your own SSH key pair
   * Please note that your compute instances in the private subnet must be built 
2. Must be built in a public subnet in a VCN
3. 

## Accessing your private compute instances 

## Issues recording and resolution
