# Deploy WikiJS in K8S with existing PSQL
# Dump WikiJS
pg_dump -d wikijs -h localhost -c -U postgres > dump_`date +%d-%m-%Y"_"%H_%M_%S`.sql

# Restore Wikijs
cat your_dump.sql |  psql -U postgres
