build:
	docker build -t colonyos/notebook .
push:
	docker push colonyos/notobook 
run:
	docker run -v $(pwd):/root -it -p 18888:8888 colonyos/notebook
