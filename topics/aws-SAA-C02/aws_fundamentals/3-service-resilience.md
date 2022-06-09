<h1>Service resilience</h1>

The resilience level of a service is described at high level in one of three ways:
- Globally resilient, the service operates globally with the single db. It's one product and its data is replicated across multiple regions in AWS. This means region can fail and service continues running. IAM is an example of a global service.
- Region resilient, services which operate in a single region with one set of data per region. They usually replicate their data to multiple AZs in that region. This means that if one of the AZs fails the service can continue operating but if the region as a whole fails then the service will fail.
- AZ resilient, these are services that run from a single AZ, if the AZ that that service is provisioned into fails that service will fail.