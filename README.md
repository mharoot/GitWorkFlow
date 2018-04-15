# GitWorkFlow
For Senior Design Team, to practice and learn about git vesion control and work flow

```bash
churn number and file name
git log --all -M -C --name-only | grep -E '^(app|lib)/' | sort | uniq -c | sort | awk 'BEGIN {print "count,file"} {print $1 "," $2}'

churn number and file name w/ limiting to last n commits
git log --all -n 5000 -M -C --name-only | grep -E '^spec/models' | sort | uniq -c | sort | awk 'BEGIN {print "count,file"} {print $1 "," $2}'

graph of churn number and frequency
git log --all -M -C --name-only | grep -E '^(app|lib)/' | sort | uniq -c | sort | awk '{print $1}' | uniq -c | sort | awk 'BEGIN { print "frequency,churn_count"} { print $1,$2}'
```