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
2. Build the image instance in a public subnet
3. Use one gateway VM per compartment or VCN
4. To use a single gateway VMs across multiple project
   * Build all your instances in the same private subnet (configured through standard architecture) - simplest
   * Build project specific private subnets in the same VCN - simpler
   * Use network security rules to build SSH access between gateway VM subnet and other private subnets
5. Always SSH to private instances from Gateway instance
6. Use your own private / public SSH key pair for added security
7. Use the same API key (for multiple users) for simpler administration

### Accessing your private compute instances 

### Issues and resolution
Please contact Oracle for Research via the following channels 
1. OracleForResearchTech_ww@Oracle.com
2. Oracle for research update calls
