A organização do conteúdo é uma proposta curricular. As competências específicas do framework se apoiam na documentação do PyTorch; o recorte de arquiteturas inclui famílias também presentes em currículos de Deep Learning, como CNNs, Transformers, modelos generativos e aprendizagem autossupervisionada.

Para qualquer arquitetura estudada, aplique esta ficha:

- [ ] [B] Explicar qual problema ela resolve e qual viés indutivo utiliza.

- [ ] [I] Identificar entradas, saídas e formatos intermediários dos tensores.

- [ ] [I] Descrever a função objetivo e o procedimento de treinamento.

- [ ] [I] Implementar uma versão mínima em PyTorch.

- [ ] [A] Analisar custo computacional, consumo de memória e limitações.

- [ ] [P] Comparar com um baseline sob avaliação adequada.

- [ ] [P] Demonstrar situações de sucesso e de falha.

### 2. Núcleo de Deep Learning
### Fundamentos das redes neurais

- [ ] [B] Diferenciar ML clássico, redes neurais e Deep Learning.

- [ ] [B] Identificar neurônios, camadas, pesos, vieses e ativações.

- [ ] [B] Diferenciar camada de entrada, camadas ocultas e saída.

- [ ] [B] Explicar forward pass, função de perda e backward pass.

- [ ] [B] Diferenciar treinamento e inferência.

- [ ] [I] Explicar por que composições não lineares ampliam a capacidade do modelo.

- [ ] [I] Diferenciar profundidade, largura e quantidade de parâmetros.

- [ ] [I] Diferenciar parâmetros aprendidos, hiperparâmetros e estado do modelo.

- [ ] [I] Explicar aprendizagem de representações.

- [ ] [I] Diferenciar feature engineering e representação aprendida.

- [ ] [A] Distinguir expressividade, facilidade de otimização e generalização.

- [ ] [A] Conhecer o significado e as limitações da aproximação universal.

- [ ] [P] Identificar quando uma rede neural não é a melhor escolha.

### Redes feedforward e MLPs

- [ ] [B] Implementar um perceptron e uma MLP.

- [ ] [I] Escolher formatos de saída para regressão, classificação binária, multiclass e multilabel.

- [ ] [I] Escolher profundidade e largura sem depender apenas de tentativa aleatória.

- [ ] [I] Comparar ReLU, LeakyReLU, GELU, SiLU, sigmoid e tanh.

- [ ] [I] Investigar saturação e neurônios inativos.

- [ ] [I] Trabalhar com embeddings para atributos categóricos.

- [ ] [A] Comparar conexões sequenciais, residuais e ramificações.

- [ ] [P] Treinar uma MLP tabular e compará-la com modelos clássicos.

- [ ] [P] Inspecionar ativações e gradientes por camada.

### Funções de perda

- [ ] [B] Diferenciar perda de treinamento e métrica de avaliação.

- [ ] [I] Usar MSE, MAE e Smooth L1/Huber para regressão.

- [ ] [I] Usar CrossEntropyLoss com logits e alvos compatíveis.

- [ ] [I] Usar BCEWithLogitsLoss para classificação binária e multilabel.

- [ ] [I] Diferenciar logits, probabilidades e decisões.

- [ ] [I] Entender por que não aplicar softmax antes de CrossEntropyLoss no uso convencional.

- [ ] [I] Diferenciar weight, pos_weight e pesos por amostra.

- [ ] [I] Controlar reduction: none, mean e sum.

- [ ] [I] Ignorar posições inválidas com máscaras ou ignore_index.

- [ ] [A] Implementar perdas ponderadas e compostas.

- [ ] [A] Conhecer focal loss, Dice loss e perdas de contraste.

- [ ] [A] Estudar KL divergence e os formatos exigidos pela implementação.

- [ ] [A] Investigar escalas e conflitos entre perdas em aprendizado multitarefa.

- [ ] [P] Testar a perda em casos pequenos com resultados conhecidos.

### Backpropagation e fluxo dos gradientes

O torch.autograd é o mecanismo de diferenciação automática que sustenta o treinamento no PyTorch. Dominar seu comportamento é diferente de apenas chamar loss.backward().

- [ ] [B] Explicar backpropagation como propagação de derivadas pelo grafo.

- [ ] [I] Diferenciar diferenciação automática de diferenciação numérica e simbólica.

- [ ] [I] Explicar vanishing gradients e exploding gradients.

- [ ] [I] Relacionar ativações, inicialização e profundidade ao fluxo dos gradientes.

- [ ] [I] Investigar camadas que não recebem gradientes.

- [ ] [A] Explicar como conexões residuais alteram o caminho dos gradientes.

- [ ] [A] Investigar instabilidade provocada por operações numericamente problemáticas.

- [ ] [P] Comparar gradientes automáticos com verificações numéricas em exemplos pequenos.

### Inicialização e normalização

- [ ] [I] Diferenciar inicialização de pesos e de vieses.

- [ ] [I] Comparar Xavier/Glorot e He/Kaiming.

- [ ] [A] Entender inicialização ortogonal e inicialização específica por arquitetura.

- [ ] [I] Explicar quebra de simetria.

- [ ] [I] Usar BatchNorm, LayerNorm, GroupNorm e InstanceNorm.

- [ ] [I] Diferenciar normalização dos dados e normalização das ativações.

- [ ] [I] Entender estatísticas por batch e estatísticas acumuladas.

- [ ] [A] Investigar BatchNorm em batches pequenos e em fine-tuning.

- [ ] [A] Comparar arquiteturas pre-norm e post-norm.

- [ ] [A] Conhecer RMSNorm.

- [ ] [P] Verificar comportamento da rede em treino e avaliação.

### Otimização

- [ ] [B] Explicar atualização de parâmetros por gradientes.

- [ ] [I] Comparar SGD, momentum e Nesterov.

- [ ] [I] Comparar Adam, AdamW, RMSprop e Adagrad.

- [ ] [I] Ajustar learning rate, momentum, betas e epsilon.

- [ ] [I] Diferenciar weight decay desacoplado e penalidade L2.

- [ ] [I] Usar grupos de parâmetros com configurações diferentes.

- [ ] [I] Aplicar gradient clipping por norma ou valor.

- [ ] [I] Usar schedules constantes, decrescentes, cosine e OneCycle.

- [ ] [I] Implementar warmup.

- [ ] [A] Investigar efeitos de batch size e acumulação de gradientes.

- [ ] [A] Distinguir passos do otimizador de microbatches.

- [ ] [A] Analisar interações entre regularização, schedule e otimizador.

- [ ] [P] Ajustar hiperparâmetros com orçamento e protocolo de validação explícitos.

### Regularização e generalização

- [ ] [B] Reconhecer overfitting e underfitting em curvas de treinamento.

- [ ] [I] Usar weight decay e dropout.

- [ ] [I] Aplicar early stopping sem usar o teste final.

- [ ] [I] Conhecer label smoothing.

- [ ] [I] Aplicar data augmentation coerente com o domínio.

- [ ] [A] Conhecer mixup, CutMix e stochastic depth.

- [ ] [A] Conhecer exponential moving average dos pesos.

- [ ] [A] Conhecer stochastic weight averaging.

- [ ] [A] Investigar ruído de rótulos e memorizações.

- [ ] [A] Distinguir redução de perda de treinamento de melhoria real de generalização.

- [ ] [P] Fazer ablações para verificar quais componentes realmente ajudam.

### Dados e avaliação

- [ ] [I] Definir unidade de observação, alvo e momento da previsão.

- [ ] [I] Separar dados por tempo, entidade ou origem quando necessário.

- [ ] [I] Identificar duplicatas e quase duplicatas entre conjuntos.

- [ ] [I] Ajustar transformações aprendidas apenas no treino.

- [ ] [I] Aplicar augmentations estocásticas somente onde o protocolo permitir.

- [ ] [I] Escolher métricas por tarefa e custos dos erros.

- [ ] [I] Agregar métricas corretamente quando batches têm tamanhos diferentes.

- [ ] [A] Investigar vazamento envolvendo modelos ou embeddings pré-treinados.

- [ ] [A] Investigar sobreposição entre benchmarks e dados de pré-treinamento.

- [ ] [P] Avaliar diferentes sementes e reportar variabilidade.

- [ ] [P] Analisar erros por classe, segmento, origem e período.

- [ ] [P] Manter um conjunto de teste isolado das decisões iterativas.

### 3. Domínio do PyTorch
### Tensores e operações

- [ ] [B] Criar tensores com tensor, zeros, ones, arange e operações aleatórias.

- [ ] [B] Inspecionar shape, dtype, device e requires_grad.

- [ ] [I] Usar indexação, slicing, máscaras e operações de seleção.

- [ ] [I] Dominar broadcasting.

- [ ] [I] Diferenciar operações elemento a elemento de multiplicação matricial.

- [ ] [I] Usar matmul, bmm e einsum.

- [ ] [I] Dominar reshape, view, flatten, squeeze e unsqueeze.

- [ ] [I] Usar permute, transpose, cat e stack.

- [ ] [I] Entender reduções por dimensão.

- [ ] [I] Converter entre NumPy e PyTorch.

- [ ] [A] Entender compartilhamento de memória, views e cópias.

- [ ] [A] Entender strides e contiguidade.

- [ ] [A] Reconhecer efeitos de operações in-place.

- [ ] [P] Escrever verificações explícitas dos formatos esperados.

- [ ] [P] Evitar loops Python quando uma operação vetorizada for adequada.

### Dispositivos e tipos numéricos

- [ ] [I] Transferir modelos e tensores com .to(...).

- [ ] [I] Manter coerência de dispositivo e tipo entre entradas, alvos e parâmetros.

- [ ] [I] Diferenciar CPU, CUDA e outros backends disponíveis no ambiente.

- [ ] [I] Comparar float32, float16 e bfloat16.

- [ ] [A] Investigar overflow, underflow e perda de precisão.

- [ ] [A] Entender execução assíncrona da GPU.

- [ ] [P] Evitar transferências desnecessárias entre CPU e acelerador.

- [ ] [P] Medir tempo de GPU com sincronização ou eventos apropriados.

- [ ] [P] Detectar gargalos de transferência e incompatibilidades de backend.

### Autograd na prática

- [ ] [B] Usar requires_grad e .backward().

- [ ] [I] Inspecionar .grad e entender acumulação de gradientes.

- [ ] [I] Diferenciar tensores folha de resultados intermediários.

- [ ] [I] Usar torch.autograd.grad.

- [ ] [I] Usar detach sem confundir com cópia dos dados.

- [ ] [I] Diferenciar no_grad, inference_mode e congelamento de parâmetros.

- [ ] [A] Entender retain_graph e create_graph.

- [ ] [A] Calcular derivadas de ordem superior quando necessárias.

- [ ] [A] Usar gradcheck em operações customizadas.

- [ ] [A] Implementar torch.autograd.Function quando houver justificativa.

- [ ] [A] Conhecer torch.func, vmap, Jacobianos e Hessianas.

- [ ] [P] Detectar quebras do grafo provocadas por conversões e operações externas.

- [ ] [P] Evitar .data como atalho para manipular parâmetros.

### Construção de modelos

- [ ] [B] Criar modelos com nn.Module.

- [ ] [B] Implementar __init__ e forward.

- [ ] [I] Usar Sequential, ModuleList e ModuleDict.

- [ ] [I] Diferenciar módulos e funções de torch.nn.functional.

- [ ] [I] Registrar parâmetros e buffers corretamente.

- [ ] [I] Inspecionar parameters, named_parameters e state_dict.

- [ ] [I] Compartilhar pesos quando a arquitetura exigir.

- [ ] [I] Congelar e descongelar submódulos.

- [ ] [A] Usar hooks para inspeção e diagnóstico.

- [ ] [P] Testar saída, dispositivo, tipos e gradientes do modelo.

- [ ] [P] Separar arquitetura, configuração e lógica de treinamento.

### Dataset e DataLoader

- [ ] [B] Implementar Dataset com __len__ e __getitem__.

- [ ] [I] Diferenciar datasets map-style e IterableDataset.

- [ ] [I] Configurar batch size, shuffle e drop_last.

- [ ] [I] Implementar collate_fn para entradas de tamanho variável.

- [ ] [I] Usar samplers e batch samplers.

- [ ] [I] Usar amostragem ponderada quando apropriada.

- [ ] [I] Configurar num_workers, pin_memory e workers persistentes.

- [ ] [A] Investigar efeitos de multiprocessing e duplicação de dados.

- [ ] [A] Distribuir leitura de datasets iteráveis entre workers e processos.

- [ ] [P] Controlar sementes dos workers.

- [ ] [P] Medir tempo de leitura, transformação e entrega dos batches.

- [ ] [P] Processar datasets maiores que a memória disponível.

### Loop de treinamento

- [ ] [B] Implementar forward, loss, backward e optimizer step.

- [ ] [I] Limpar gradientes no momento correto.

- [ ] [I] Usar model.train() e model.eval().

- [ ] [I] Entender que eval() não desativa o autograd.

- [ ] [I] Implementar validação sem construção desnecessária de grafos.

- [ ] [I] Acumular métricas sem reter tensores ligados ao grafo.

- [ ] [I] Implementar gradient accumulation com escala correta da perda.

- [ ] [I] Atualizar schedulers na frequência apropriada.

- [ ] [I] Implementar early stopping e seleção do melhor checkpoint.

- [ ] [P] Registrar perdas, métricas, learning rate e tempo.

- [ ] [P] Retomar treinamento a partir de um checkpoint.

- [ ] [P] Tratar interrupções e falhas sem perder todo o experimento.

### Debugging e testes

- [ ] [I] Fazer a rede memorizar um pequeno conjunto de exemplos.

- [ ] [I] Testar uma única iteração de treinamento.

- [ ] [I] Inspecionar valores NaN e Inf.

- [ ] [I] Verificar se parâmetros mudam após optimizer.step().

- [ ] [I] Verificar se parâmetros congelados permanecem inalterados.

- [ ] [I] Inspecionar normas dos gradientes e distribuição de ativações.

- [ ] [A] Usar detecção de anomalias do autograd quando necessário.

- [ ] [P] Testar máscaras, padding e losses manualmente em exemplos pequenos.

- [ ] [P] Testar batches de tamanho um e batches incompletos.

- [ ] [P] Testar consistência entre inferência individual e em lote.

- [ ] [P] Escrever testes para checkpoints e retomada.

- [ ] [P] Identificar se o problema está nos dados, no modelo ou no loop.

### Precisão mista

A API torch.amp combina autocast e, quando necessário, escalonamento de gradientes. O escalonamento é especialmente relevante para reduzir underflow de gradientes em treinamento com float16.

- [ ] [I] Usar torch.autocast.

- [ ] [I] Usar torch.amp.GradScaler quando adequado.

- [ ] [I] Comparar treinamento em FP32, FP16 e BF16.

- [ ] [A] Entender quais operações exigem maior precisão.

- [ ] [A] Aplicar clipping depois de remover a escala dos gradientes.

- [ ] [A] Integrar AMP com gradient accumulation.

- [ ] [P] Comparar qualidade, velocidade e memória antes e depois de AMP.

- [ ] [P] Salvar o estado do scaler para retomada.

### Desempenho e memória

- [ ] [I] Distinguir memória de parâmetros, gradientes, ativações e otimizador.

- [ ] [I] Identificar retenção acidental de grafos.

- [ ] [I] Usar ferramentas de profiling do PyTorch.

- [ ] [I] Identificar gargalos de CPU, GPU, armazenamento e DataLoader.

- [ ] [A] Conhecer formatos de memória como channels-last.

- [ ] [A] Usar activation checkpointing quando apropriado.

- [ ] [A] Diferenciar activation checkpointing de salvar checkpoints em disco.

- [ ] [P] Medir throughput e latência com warmup.

- [ ] [P] Investigar erros de falta de memória sem recorrer apenas a reduzir batch size.

- [ ] [P] Avaliar o custo das otimizações em complexidade e qualidade.

Activation checkpointing reduz memória de ativações à custa de recomputar partes do forward durante o backward; não é um mecanismo de persistência do modelo.

### Compilação e exportação

torch.compile busca acelerar a execução; torch.export serve à captura de uma representação do programa para fluxos de transformação e execução posteriores. São ferramentas com objetivos distintos.

- [ ] [I] Comparar execução eager e torch.compile.

- [ ] [A] Entender graph breaks e recompilações.

- [ ] [A] Investigar shapes dinâmicos e especialização.

- [ ] [A] Avaliar interação entre compilação, precisão mista e autograd.

- [ ] [P] Separar tempo inicial de compilação do desempenho em regime estável.

- [ ] [P] Verificar equivalência numérica dentro de tolerâncias apropriadas.

- [ ] [A] Conhecer torch.export.

- [ ] [P] Avaliar exportação para ONNX quando o destino exigir.

- [ ] [P] Verificar operadores suportados e limitações do ambiente de execução.

### Treinamento distribuído

- [ ] [I] Diferenciar paralelismo de dados, de modelo e de pipeline.

- [ ] [I] Entender rank, world size e comunicação entre processos.

- [ ] [I] Usar DistributedDataParallel.

- [ ] [I] Distribuir amostras corretamente entre processos.

- [ ] [I] Atualizar o sampler por época quando necessário.

- [ ] [A] Diferenciar batch local e batch global.

- [ ] [A] Entender sincronização e redução de gradientes.

- [ ] [A] Conhecer FSDP e sharding de parâmetros, gradientes e estados.

- [ ] [A] Conhecer tensor parallelism e sequence parallelism.

- [ ] [P] Agregar métricas sem duplicação de amostras.

- [ ] [P] Diagnosticar travamentos e problemas de comunicação.

- [ ] [P] Salvar e retomar checkpoints distribuídos.

- [ ] [P] Medir ganho real de escala.

O Distributed Checkpoint do PyTorch contempla estados distribuídos e permite re-sharding ao carregar em topologias diferentes, dentro das condições suportadas pelo mecanismo.

### Reprodutibilidade e persistência

Sementes ajudam a controlar aleatoriedade, mas não garantem resultados idênticos entre versões, plataformas ou CPU e GPU. A documentação recomenda tratar reprodutibilidade como uma propriedade do ambiente e do experimento completo.

- [ ] [I] Controlar sementes de Python, NumPy e PyTorch.

- [ ] [I] Controlar aleatoriedade dos workers e dos samplers.

- [ ] [A] Conhecer algoritmos determinísticos e seus custos.

- [ ] [P] Registrar versões, hardware, dados e configuração.

- [ ] [P] Salvar state_dict do modelo.

- [ ] [P] Salvar otimizador, scheduler, scaler, etapa e estado aleatório quando necessário.

- [ ] [P] Registrar arquitetura, vocabulário e pré-processamento junto do artefato.

- [ ] [P] Usar map_location e verificar compatibilidade ao carregar.

- [ ] [P] Testar carregamento em um processo novo.

- [ ] [P] Tratar checkpoints externos como artefatos potencialmente perigosos.

Para compatibilidade, a documentação recomenda salvar o state_dict em vez de serializar diretamente o módulo inteiro. Esse estado inclui parâmetros e buffers persistentes.

### 4. Arquiteturas e especializações
Os blocos seguintes ampliam o núcleo: não são pré-requisitos para começar a construir projetos. CNNs, Transformers, modelos autossupervisionados e generativos aparecem juntos em currículos de visão modernos, mas cada família exige sua própria prática e avaliação.

### Redes convolucionais

- [ ] [B] Explicar convolução, filtros, canais e mapas de ativação.

- [ ] [I] Calcular formatos de saída considerando kernel, padding, stride e dilation.

- [ ] [I] Usar convoluções 1D, 2D e 3D.

- [ ] [I] Diferenciar convolução convencional, agrupada e depthwise separable.

- [ ] [I] Usar max pooling, average pooling e adaptive pooling.

- [ ] [I] Entender campo receptivo.

- [ ] [I] Implementar blocos residuais.

- [ ] [A] Diferenciar convolução transposta de inversão de convolução.

- [ ] [A] Investigar artefatos de upsampling.

- [ ] [I] Estudar famílias como ResNet, DenseNet, MobileNet, EfficientNet e ConvNeXt.

- [ ] [P] Implementar uma CNN do zero e adaptar uma pré-treinada.

### Visão computacional

- [ ] [I] Construir pipelines de imagens com torchvision.

- [ ] [I] Aplicar normalização compatível com modelos pré-treinados.

- [ ] [I] Diferenciar classificação, detecção e segmentação.

- [ ] [I] Tratar localização, bounding boxes e máscaras.

- [ ] [I] Estudar IoU, AP/mAP e métricas de segmentação.

- [ ] [A] Estudar detectores de uma e duas etapas.

- [ ] [A] Estudar U-Net e arquiteturas encoder–decoder.

- [ ] [A] Estudar segmentação semântica, de instâncias e panóptica.

- [ ] [A] Estudar estimation de pose, profundidade e optical flow.

- [ ] [A] Conhecer modelos para vídeo e dados 3D.

- [ ] [P] Avaliar erros por tamanho do objeto, classe e condição de captura.

- [ ] [P] Aplicar augmentations preservando rótulos, caixas e máscaras.

### Redes recorrentes e sequências

- [ ] [I] Implementar RNN, LSTM e GRU.

- [ ] [I] Diferenciar hidden state e cell state.

- [ ] [I] Trabalhar com redes bidirecionais e multicamadas.

- [ ] [I] Tratar sequências de tamanho variável.

- [ ] [I] Usar padding, comprimentos e sequências empacotadas.

- [ ] [A] Entender backpropagation through time.

- [ ] [A] Implementar truncated BPTT.

- [ ] [A] Estudar teacher forcing e exposure bias.

- [ ] [I] Implementar modelos seq2seq.

- [ ] [P] Comparar recorrência com convoluções temporais e atenção.

### Atenção e Transformers

- [ ] [B] Explicar atenção como combinação dependente do conteúdo.

- [ ] [I] Identificar queries, keys e values.

- [ ] [I] Implementar scaled dot-product attention.

- [ ] [I] Implementar multi-head attention.

- [ ] [I] Diferenciar self-attention e cross-attention.

- [ ] [I] Construir máscaras de padding e máscaras causais.

- [ ] [I] Entender positional encodings e embeddings posicionais.

- [ ] [A] Estudar posições relativas e RoPE.

- [ ] [I] Implementar blocos encoder e decoder.

- [ ] [A] Comparar encoder-only, decoder-only e encoder–decoder.

- [ ] [A] Estudar custo de atenção em função do comprimento.

- [ ] [A] Conhecer atenção eficiente e kernels otimizados.

- [ ] [A] Estudar multi-query e grouped-query attention.

- [ ] [P] Testar máscaras, shapes e ausência de acesso a tokens futuros.

- [ ] [P] Comparar implementação própria com módulos existentes.

### NLP e modelos de linguagem

- [ ] [I] Diferenciar caracteres, palavras, subwords e tokens especiais.

- [ ] [I] Estudar BPE, WordPiece e tokenização baseada em Unigram.

- [ ] [I] Construir embeddings e tratar padding.

- [ ] [I] Formular tarefas de classificação, tagging e geração.

- [ ] [I] Estudar masked language modeling e causal language modeling.

- [ ] [I] Implementar deslocamento correto de entradas e alvos.

- [ ] [I] Calcular loss por token válido e perplexidade.

- [ ] [A] Entender limitações da comparação de perplexidade entre tokenizadores.

- [ ] [I] Comparar greedy decoding, beam search e sampling.

- [ ] [I] Ajustar temperatura, top-k e top-p.

- [ ] [A] Estudar KV cache e diferenças entre prefill e decoding.

- [ ] [P] Treinar um pequeno modelo autoregressivo.

- [ ] [P] Avaliar qualidade, repetição, factualidade e falhas por tarefa.

### Transfer learning e fine-tuning

- [ ] [I] Diferenciar treinamento do zero, extração de atributos e fine-tuning.

- [ ] [I] Substituir cabeças de saída.

- [ ] [I] Congelar e descongelar camadas.

- [ ] [I] Usar learning rates diferentes por grupo de parâmetros.

- [ ] [A] Investigar catastrophic forgetting.

- [ ] [A] Estudar adapters e LoRA.

- [ ] [A] Conhecer fine-tuning eficiente com modelos quantizados.

- [ ] [A] Diferenciar continued pretraining e supervised fine-tuning.

- [ ] [P] Verificar tokenizer, normalização e template de entrada.

- [ ] [P] Comparar fine-tuning com uso do modelo sem adaptação.

- [ ] [P] Avaliar perdas de capacidade em tarefas não usadas na adaptação.

### Aprendizagem autossupervisionada e representações

- [ ] [I] Diferenciar supervisão externa de objetivos gerados a partir dos dados.

- [ ] [I] Estudar contrastive learning.

- [ ] [I] Entender pares positivos, negativos e temperatura.

- [ ] [A] Estudar SimCLR e MoCo.

- [ ] [A] Estudar métodos sem negativos, como BYOL e SimSiam.

- [ ] [A] Estudar distilação autossupervisionada e DINO.

- [ ] [A] Estudar masked autoencoders.

- [ ] [A] Investigar colapso de representações.

- [ ] [P] Avaliar embeddings com linear probing e fine-tuning.

- [ ] [P] Avaliar recuperação, transferência e robustez das representações.

### Autoencoders

- [ ] [I] Implementar encoder, bottleneck e decoder.

- [ ] [I] Construir autoencoders densos e convolucionais.

- [ ] [I] Estudar denoising e sparse autoencoders.

- [ ] [A] Investigar representação latente e capacidade de reconstrução.

- [ ] [A] Conhecer vector-quantized autoencoders.

- [ ] [P] Avaliar reconstrução e utilidade da representação separadamente.

- [ ] [P] Investigar limites do uso de erro de reconstrução para anomalias.

### Modelos generativos

- [ ] [B] Diferenciar geração de dados e discriminação.

- [ ] [I] Diferenciar modelos condicionais e não condicionais.

- [ ] [I] Implementar um Variational Autoencoder.

- [ ] [A] Entender reparametrização, ELBO e posterior collapse.

- [ ] [I] Implementar uma GAN simples.

- [ ] [A] Investigar instabilidade, mode collapse e equilíbrio entre redes.

- [ ] [A] Estudar WGAN e gradient penalty.

- [ ] [A] Estudar normalizing flows e transformações invertíveis.

- [ ] [A] Estudar modelos autoregressivos.

- [ ] [A] Conhecer energy-based models.

- [ ] [P] Avaliar qualidade, diversidade, cobertura e memorização.

- [ ] [P] Não reduzir a avaliação generativa a uma única métrica.

### Difusão e flow matching

- [ ] [I] Explicar processo de adição e remoção de ruído.

- [ ] [I] Implementar uma difusão simples.

- [ ] [I] Entender noise schedules e condicionamento temporal.

- [ ] [A] Comparar parametrizações de predição de ruído, amostra e velocidade.

- [ ] [A] Estudar DDPM e DDIM.

- [ ] [A] Estudar modelos score-based.

- [ ] [A] Entender classifier-free guidance.

- [ ] [A] Estudar latent diffusion.

- [ ] [A] Estudar flow matching e rectified flows.

- [ ] [P] Comparar qualidade e custo com diferentes samplers e números de passos.

- [ ] [P] Avaliar geração condicionada e preservação de atributos desejados.

### Modelos multimodais

- [ ] [I] Diferenciar fusão precoce, tardia e por atenção.

- [ ] [I] Construir embeddings de diferentes modalidades.

- [ ] [A] Estudar alinhamento contrastivo imagem–texto.

- [ ] [A] Estudar CLIP e modelos de captioning.

- [ ] [A] Entender encoders, projetores e integração com modelos de linguagem.

- [ ] [P] Avaliar recuperação entre modalidades.

- [ ] [P] Avaliar grounding e erros de associação.

- [ ] [P] Testar ausência, corrupção e conflito entre modalidades.

### Áudio e fala

- [ ] [I] Trabalhar com waveform, frequência de amostragem e canais.

- [ ] [I] Construir espectrogramas e representações mel.

- [ ] [I] Tratar sequências de durações variáveis.

- [ ] [I] Diferenciar classificação de áudio, ASR e TTS.

- [ ] [A] Estudar CTC e alinhamento entre áudio e texto.

- [ ] [A] Estudar modelos de áudio autossupervisionados.

- [ ] [A] Conhecer vocoders neurais e separação de fontes.

- [ ] [P] Avaliar WER/CER e desempenho por condição acústica.

- [ ] [P] Construir augmentations coerentes com a tarefa.

### Séries temporais

- [ ] [I] Construir janelas, lags, horizontes e alvos temporais.

- [ ] [I] Implementar CNNs temporais, RNNs e Transformers para séries.

- [ ] [I] Diferenciar previsão univariada e multivariada.

- [ ] [A] Comparar previsão direta, recursiva e multi-horizonte.

- [ ] [A] Estudar modelos globais e embeddings de séries.

- [ ] [A] Estudar previsão probabilística e quantílica.

- [ ] [P] Realizar backtesting sem informação futura.

- [ ] [P] Comparar com baselines ingênuos e modelos clássicos.

- [ ] [P] Avaliar por série, período e horizonte.

### Redes neurais em grafos

- [ ] [B] Identificar nós, arestas e atributos.

- [ ] [I] Diferenciar tarefas em nós, arestas e grafos.

- [ ] [I] Explicar message passing e agregação.

- [ ] [I] Estudar GCN, GraphSAGE e GAT.

- [ ] [A] Diferenciar aprendizagem transdutiva e indutiva.

- [ ] [A] Investigar oversmoothing e oversquashing.

- [ ] [A] Estudar amostragem de vizinhanças.

- [ ] [P] Usar uma biblioteca de grafos compatível com PyTorch.

- [ ] [P] Avaliar leakage estrutural e disponibilidade das arestas.

### Deep Reinforcement Learning

- [ ] [I] Revisar agente, ambiente, ação, estado e recompensa.

- [ ] [I] Diferenciar on-policy e off-policy.

- [ ] [I] Implementar DQN e entender replay buffer e target network.

- [ ] [A] Estudar Double DQN e Dueling DQN.

- [ ] [I] Estudar policy gradients e actor–critic.

- [ ] [A] Estudar PPO e SAC.

- [ ] [A] Conhecer aprendizado por imitação e offline RL.

- [ ] [P] Avaliar múltiplas sementes e eficiência amostral.

- [ ] [P] Investigar reward hacking e instabilidade.

- [ ] [P] Separar desempenho de treinamento e avaliação.

### Especializações de pesquisa

- [ ] [A] Estudar mixture-of-experts e roteamento.

- [ ] [A] Estudar modelos de espaço de estados e arquiteturas híbridas.

- [ ] [A] Estudar aprendizagem contínua e esquecimento catastrófico.

- [ ] [A] Estudar meta-learning e few-shot learning.

- [ ] [A] Estudar aprendizagem multitarefa e conflito de gradientes.

- [ ] [A] Estudar deep ensembles e redes bayesianas.

- [ ] [A] Conhecer neural ODEs.

- [ ] [A] Conhecer physics-informed neural networks e neural operators.

- [ ] [A] Conhecer redes equivariantes.

- [ ] [A] Conhecer implicit neural representations e neural rendering.

- [ ] [P] Selecionar aprofundamentos orientados por problemas, não apenas pela novidade.

### 5. Produção e comprovação
### Compressão e inferência eficiente

- [ ] [I] Diferenciar redução de parâmetros e redução efetiva de latência.

- [ ] [I] Estudar quantização pós-treinamento e quantization-aware training.

- [ ] [A] Diferenciar quantização de pesos e de ativações.

- [ ] [A] Comparar quantização por tensor e por canal.

- [ ] [A] Estudar pruning estruturado e não estruturado.

- [ ] [A] Estudar knowledge distillation.

- [ ] [P] Avaliar qualidade após compressão.

- [ ] [P] Medir ganhos no hardware e runtime de destino.

- [ ] [P] Escolher ferramentas de quantização conforme a versão e o backend suportados.

### Robustez, incerteza e interpretabilidade

- [ ] [I] Avaliar confiança e calibração das probabilidades.

- [ ] [I] Conhecer temperature scaling.

- [ ] [A] Estudar incerteza epistemológica e aleatória.

- [ ] [A] Comparar ensembles e aproximações baseadas em dropout.

- [ ] [A] Estudar detecção de entradas fora da distribuição.

- [ ] [A] Investigar robustness a corrupções e mudanças de domínio.

- [ ] [A] Conhecer ataques adversariais e defesas.

- [ ] [I] Inspecionar saliency maps e Grad-CAM.

- [ ] [A] Conhecer Integrated Gradients.

- [ ] [A] Investigar estabilidade e limitações das explicações.

- [ ] [P] Não tratar atenção ou mapas de saliência como prova causal.

- [ ] [P] Definir critérios de abstinência e revisão humana.

### Segurança e responsabilidade

- [ ] [I] Investigar vieses nos dados e nos rótulos.

- [ ] [A] Estudar memorização e exposição de informações sensíveis.

- [ ] [A] Conhecer membership inference e model extraction.

- [ ] [A] Conhecer aprendizado federado e privacidade diferencial.

- [ ] [P] Verificar origem, licença e permissões de uso dos dados e modelos.

- [ ] [P] Avaliar resultados por grupos relevantes.

- [ ] [P] Documentar usos inadequados e limitações.

- [ ] [P] Definir responsáveis, supervisão e procedimentos de incidentes.

### Engenharia de experimentos

- [ ] [P] Organizar configurações, código, dados e artefatos.

- [ ] [P] Registrar hiperparâmetros e versão do dataset.

- [ ] [P] Manter um baseline reproduzível.

- [ ] [P] Registrar hipóteses antes de experimentos caros.

- [ ] [P] Fazer ablações de arquitetura, perda, dados e regularização.

- [ ] [P] Comparar modelos sob orçamento computacional explícito.

- [ ] [P] Registrar resultados negativos e falhas.

- [ ] [P] Evitar selecionar apenas a melhor semente.

- [ ] [P] Reproduzir resultados em ambiente limpo.

- [ ] [P] Produzir relatórios com resultados, custos e limitações.

### Deployment e manutenção

- [ ] [P] Empacotar modelo e pré-processamento.

- [ ] [P] Definir contrato de entrada e saída.

- [ ] [P] Validar tipos, formatos, comprimentos e limites.

- [ ] [P] Implementar inferência em lote e individual.

- [ ] [P] Usar eval() e um modo adequado de inferência.

- [ ] [P] Medir latência p50, p95 e p99 quando pertinente.

- [ ] [P] Controlar concorrência, memória e tamanho de batches.

- [ ] [P] Implementar warmup quando necessário.

- [ ] [P] Monitorar erros operacionais e distribuição das entradas.

- [ ] [P] Monitorar desempenho quando rótulos se tornarem disponíveis.

- [ ] [P] Definir atualização, rollback e critérios de descontinuação.

- [ ] [P] Testar equivalência entre ambiente de pesquisa e ambiente de operação.

### Leitura e reprodução de artigos

- [ ] [I] Identificar problema, hipótese, contribuição e baselines.

- [ ] [I] Reconstruir o fluxo de tensores da arquitetura.

- [ ] [I] Identificar objetivos, dados e protocolo de avaliação.

- [ ] [A] Investigar detalhes omitidos e dependências do resultado.

- [ ] [A] Diferenciar reprodução do código original e reimplementação independente.

- [ ] [P] Reproduzir uma versão reduzida do experimento.

- [ ] [P] Comparar resultados considerando orçamento e condições diferentes.

- [ ] [P] Documentar divergências sem atribuí-las automaticamente a erro próprio.

### Evidências de domínio

Para não transformar o checklist em uma lista de aulas assistidas, marque um tópico como concluído somente quando conseguir:

Explicá-lo sem consultar o material.

Implementar um exemplo mínimo.

Interpretar o comportamento do modelo.

Mostrar pelo menos uma situação de falha.

Comparar com uma alternativa.

Registrar o experimento de maneira reproduzível.