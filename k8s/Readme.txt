Below is an example of a complete set of YAML definitions that includes:

A custom namespace (my-app-namespace)
The my-app-deployment (labeled with app: my-app)
The cache-deployment (labeled with app: cache)
The my-app-service exposing the my-app-deployment
The NetworkPolicy that restricts traffic for the my-app-deployment pods according to your specifications
Note:

The NetworkPolicy allows ingress from:
All pods within the same namespace (using an empty podSelector), and
Any pod (regardless of namespace) with the label app: trusted.
It allows egress only to pods within the same namespace.
Any traffic not explicitly allowed by these rules is denied.
