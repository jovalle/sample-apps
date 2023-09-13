# jobs-app

From an Isovalent lab. Useful for testing and experimentation outside of the lab setting.

It is asssumed Cilium is installed with Hubble enabled.

## Deploy

```sh
helm upgrade jobs-app ./helm/jobs-app.tgz \
    --namespace tenant-jobs \
    --reuse-values \
    --set crawler.replicas=3 \
    --set crawler.crawlFrequencyLowerBound=0.2 \
    --set crawler.crawlFrequencyUpperBound=0.5 \
    --set resumes.replicas=2
```

