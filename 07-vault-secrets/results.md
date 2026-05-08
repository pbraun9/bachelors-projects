# vault

oh oh oh, yandex disk for once!  how wonderful) ^^
-- that is a good and _safer_ habit indeed.

some unnecessary focus on seal/unseal as this only helps very specific corner-cases (if ever the store gets stolen)
-- as it is usually online and unlocked/alive in view to be used as a service.
I mean, why not, but then you should explain what sealing protect against exactly.

ok good ACL policies are in place

nice general demo (ssd-general-demo.mp4)
-- checking the envs within the pods

ok I didn't use vault agent injector myself.
I use it by other means.
it seems that's an excellent practice as for K8S.
however, I suppose even for K8S, let CI/CD authenticate to Vault,
fetch secrets, and inject them int pods during deployment is also fine.

my opinion is that is complicates the infra a bit (additional sidecar containers),
but all good, what you did is considered best practice.

good job overall, congrats

