# iac-birthday-tracker

## ci/cd

overall looks more than complete, just some remarks:

it's quite inefficient to re-install tools over and over again during pipelines,
takes time and consumes resources for no reason,
best is to have runners with all the tools available (eventually with dedicated IaC for themselves)

it might also be worth considering doing the chechov security scanning outside of pipelines in case it slows them down

## tf

interesting technique, all goes into tf user-data \#cloud-config with packages, write_files and runcmd.  good job, as the alternatives are very painful and as far as I experienced, inefficient: making a link between terraform and ansible for example is not trivial

seems complete, all the pieces are there even grafana dashboards as code!

## secrets mgmt

this is not well documented (missing screenshot on TF Cloud UI), all there is is a slide "Workspace variables" and README.md 3.2 Hardened Secrets.  I asked during presentation and you answered about Terraform Cloud UI

ok there is a difference in the code between casual variables and sensitive variables

## data persistence

one possible weak point of this IaC deployed app is its persistent data.
is that data only located in the db?
where is the data physically located?
what happens in case we loose the VM?

those considerations were not necessary without IaC, but since IaC handles VMs almost in a similar way as Pods, then we need to make sure we keep track of the Volumes somehow.

## docs

nice explanations on how ci/cd interacts with terraform,
here apply on merge

fwiw there is an alternative to terraform/terragrunt apply-on-merge with Atlantis (https://www.runatlantis.io/) and other even more recent tools I can't recall:
it is possible to apply interactively before merge

---

UPDATE: weakness of using `#cloud-config` is that it is not re-usable.
it's only one-shot during initial deploy...
the \#cloud-config user-data technique is not scalable,
it has no conf mgmt nor maintainance capability.

