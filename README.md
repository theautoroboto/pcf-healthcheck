# pcf-healthcheck
Repo to share my method of a healthcheck concourse pipeline

## EXAMPLE
- Simple healthcheck, not scheduled

fly -t pxa sp -p health-check-verbose -c pipelines/pipeline.yml -l configs/pipeline-params.yml -y trigger-schedule=false -y VERBOSE_TEST=true -n

- Verbose healthcheck, scheduled.  This runs all smoketests

fly -t pxa sp -p health-check -c pipelines/pipeline.yml -l configs/pipeline-params.yml -y trigger-schedule=true -y VERBOSE_TEST=false -n
