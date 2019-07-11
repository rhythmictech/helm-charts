# Helm Charts
Rhythmic Technologies helm charts 

## Getting Started 

### Adding a Chart
First, create a new chart in the `charts` directory:
```
# add you chart's folder and create your chart
$ cd charts
$ helm create mynewchart
```

Then `package` that chart with `helm`:
```
# build the zip file 
$ helm package charts/mynewchart

# update the index.yaml file 
$ helm repo index .
```

Then add it all to git:
```
# add it all to git
$ git add mynewchart-* index.yaml charts/mynewchart/*
$ git commit -m 'New chart mynewchart'
$ git push
```

### Using a Chart

Add this repository to helm, update your repos, and pull down any of the charts. 
```
$ helm repo add rhythmictech https://rhythmictech.github.io/helm-charts/

$ helm repo update

$ helm repo search mynewchart
```

## Charts

### AWX 
Helm chart for AWX, upstream of Ansible Tower. 
- https://github.com/ansible/awx
- https://github.com/Najeongho/charts/tree/master/incubator/awx
