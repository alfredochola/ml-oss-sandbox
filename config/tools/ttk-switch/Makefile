NAMESPACE=ml-app
CHART=mojaloop/ml-testing-toolkit
RELEASE_NAME=ttk-switch

up:
	helm upgrade --install --namespace ${NAMESPACE} ${RELEASE_NAME} ${CHART} --values ./values.yaml
	kubectl apply -f ./ingress.yaml

down:
	kubectl delete -f ./ingress.yaml
	helm del ${RELEASE_NAME}

health:
	@echo 'TODO! - this service doesnt expose any health checks'