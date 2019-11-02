# orf2019 add ymal

## /manifests/grafana-service.yaml

### add spec: externalIPs:

apiVersion: v1
kind: Service
metadata:
  labels:
    app: grafana
  name: grafana
  namespace: monitoring
spec:
  externalIPs:
  - xxx.xxx.xxx.xxx
  ports:
  - name: http
    port: 3000
    targetPort: http
  selector:
    app: grafana
    
