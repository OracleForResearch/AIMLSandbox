## Using the Research Gatway Image

### Overview
The Research gateway image provides a secure gateway to your researech tenancy.Some of the other usages are described below.
1. Secure gateway: Provides a secure gateway with A simple deployment. Prevents direct access to your private compute cluster and databases. 
2. Build: Should be built in a public subnet (default)
3. Architecture: Recommended to create on Oracle for Research standard architecture
4. OCI-CLI: Pre-installed version of OCI Command line interface (CLI) Tools
5. Configurable: Easily configurable to your tenancy environment
6. Operating system: Oracle Linux operating systems

### Tools and scripts 
1. Following scripts are included with the image
   * OCI-CLI object list scripts (list compartment, instances, images)
   * Instance Terminating and startup scripts
   * Block storage attachment and detachment
   * SSH to login to VM in your private subnet
   * Standard Linux monitoring examples (upcoming)
   * Using OCI Telemetry monitoring with OCI-CLI (upcoming)
   * Using NVIDIA monitoring tools with OCI-CLI (upcoming)

### Downloading and using the Image
1. Implement the Oracle for Research standard architecture
   * Create a new compartment
   * Implement a new VCN in the compartment through the VCN creation wizard
2. Import and create a custom image from the [Oracle for Research URL]()
3. Create a free-tier compute instance with the custom image in the public subnet
   * Please generate SSH key (easier if you are starting out) or use your own keys while building the instance.

### Configuring OCI CLI
OCI CLI needs some configuration to successfully work with your tenancy and the user working with it. Please follow the steps below.
1. Login to your OCI tenancy console
2. Get the Tenancy OCID
3. Get the user OCID
4. Setup the API Public key
   * SSH to Research Gateway VM
   * Go to ~/.oci

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
