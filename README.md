# dio-kafka-example
Some simple examples for my presentation.

	# Mensageria
		Sistemas distribuídos que se comunicam por troca de mensagens(eventos) atravéz de um Message Broker
		
		-Message Broker/Barramento de mensagem(ou Event backbone)
			Servidor de mensagens responsável por garantir o enfileiramento, armazenamento até que um consumidor retire e seja efetuada a entrega das mensagens
			
	# Arquitetura baseada em eventos
	
		-Prioridades da Aruitetura em eventos
		
			Premissa: 
				Dados transitanto
			Função: 
				Responder a eventos
			Fonte da verdade: 
				Log de eventos
			Objetivo: 
				Sistema nervoso do negócio
			
		-Prioridades da arquitetura tradicional
		
			Premissa: 
				Dados seguros
			Função: 
				Preservar os dados
			Fonte da verdade: 
				base de dados
			Objetivo: 
				Funcionar como repositório de dados
				
				
	# Padrões de mensageria
	
		-Fire and forget
			Remetente ignora recebimento
		
		-Request/Reply
			Remetente aguarda resposta
			
		-Publisher/Subscriber pubsub
			Mensagem enviada e entregue a todos os inscritos
			
	# Persistência e Durabilidade
	
		-Configurável
			Política de descarte de mensagens
			
	#Streaming de eventos
				
		-O que é?
			Fluxo de eventos
			Captura de dados em tempo real
		
			Características:
			
				-Durabilidade
					Armazenamento de forma duradoura
				
				-Tratamento
					Manipular, processar e reagir aos fluxos
					
				-Destinação
					encaminhar fluxo de eventos 
					
				-Garantia
					Garante um fluxo contínuo e interpretação dos dados para que informações estejam no lugar certo na hora certa
					
	# Sistemas de mensageria disponíveis no mercado
		
		-RabbitMQ
			Open Source mais utilizado 
		
		-Kafka
			Plataforma distribuída, open source desenvolvida em java, de streaming de eventos
			
			Características:
				Alto throughput, disponibilidade, escalável, armazenamento permanente, fault-tolerant
				
			Schema registry
				Validação das mensagens a partir das premissas que produtores e consumidores usam o mesmo padrão baseado em array de bytes
		
		-Amazon Simple Notification Service(SNS)
			Serviço de mensagens gerenciado baseado em PUSH
			
			Aplicação para aplicação(A2A)
				usando tópicos, repassa para sistemas consumidores como Amazon SQS, AWS Lambda, Endpoints HTTPS entre outros
			
			Aplicação para pessoa(A2P)
				envio SMS, email, push de apps
		
		-Amazon Simple Queue Service(SQS)
			Serviço de filas de mensagens, limite de 7 dias, baseado em PULL
			
	# Vantagens
		
		-Comunicação ininterrupta
			Produtor pode enviar mensagens independente do consumidor estar ativo ou não e vice-versa
		
		-Desempenho
			Filas que demandam mais desempenho podem ter mais consumidores melhorando a experiência do usuário processando paralelamente
		
		-Confiança
			Mecanismos de retentativa de entrega em caso de falha do consumidor ou roteamento de mensagens não entregues(dead-letter queue)
		
	# Desvantagens
		
		-Complexidade
			Broker precisa ser bem configurado
			
		-Inconsistência Eventual
			Algum componente pode não ter o dado em sua versao mais atualizada até que os eventos sejam propagados
			
		-Debugging dificil
			Cada serviço tem seu proprio logging
			
		-Curva de aprendizado
			Dificuldade de comessar a trabalhar com eles pela necessidade de diversas configurações que precisam ser refinadas para cada caso de uso
		
			
			
		
	
		
		
	
