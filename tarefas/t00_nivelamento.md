# Tarefa 0: Estudo Inicial

## Objetivo

Permitir que todos os membros do projeto estejam no mesmo ponto de partida para o início das atividades. Queremos entender:

1. Como medir o consumo de energia de uma GPU.
2. Básico de redes neurais.
3. Básico das técnicas de otimização de redes neurais: quantização e poda.

Ninguém precisa dominar tudo, a meta é termos uma ideia inicial do tema para que possamos dividir futuramente o projeto em duas frentes principais: **otimização de modelos de IA** e **medição do consumo de energia em GPU**.

Nosso foco é o gasto de energia na inferência (usar modelos já treinados) em uma GPU RTX 4090: medir esse gasto e reduzi-lo.

## O que fazer?

Estude os materiais indicados abaixo. Sinta-se livre para buscar por outros materiais complementares. 

### Como medir o consumo de energia de uma GPU?

1. [Energy vs power](https://energyeducation.ca/encyclopedia/Energy_vs_power). Diferença de potência e energia. Estamos interessados no consumo de energia.

2. [An experimental comparison of software-based power meters: focus on CPU and GPU.](https://perso.ens-lyon.fr/laurent.lefevre/pdf/CCGRID2023_Ostapenco_Jay_Lefevre.pdf) É um artigo científico. Leia só a seção II-A, “Methods to measure the energy consumption”, até o item “b) Nvidia GPU NVML” inclusive, e pare em “4) Power and energy modeling”. Mostra as formas de medir energia, de medidores de tomada a sensores dentro do computador. Dê foco para as seções "Hardware sensors and software interfaces" e "NVML", que é o que utilizaremos.

3. [Measuring GPU Energy: Best Practices](https://ml.energy/blog/energy/measurement/measuring-gpu-energy-best-practices/) É a leitura mais importante deste bloco. Explica por que devemos medir em vez de estimar, as duas formas de medir (amostrar a potência ou ler um contador de energia acumulada). Pode ignorar a parte do Zeus Monitor.

4. **Para quem quiser se aprofundar**

Os materiais sobre medição de energia em GPU são densos, e quase tudo foi escrito para especialistas. Por isso os materiais acima são introdutórios de propósito. Quem se interessar pela medição pode ler o artigo abaixo. Ele é técnico, mas curto, e trata exatamente do que vamos estudar: as duas formas de ler a energia no NVML (potência e contador de energia).

- [Evaluating the Influence of Measurement Frequency on Energy Readings Using Intel RAPL and NVIDIA NVML](https://hotcarbon.org/assets/2026/paper-46.pdf)

### Básico de Redes Neurais

1. [O que é uma rede neural? (20 min)](https://www.youtube.com/watch?v=aircAruvnKk&list=PLZHQObOWTQDNU6R1_67000Dx_ZCJB-3pi&index=1) 

2. [LLMs explicados resumidamente (7 min)](https://www.youtube.com/watch?v=LPZh9BOjkQs&list=PLZHQObOWTQDNU6R1_67000Dx_ZCJB-3pi&index=5)

### Técnicas de Otimização
Abaixo coloquei três videoaulas introdutórias para duas técnicas muito conhecidas de otimização de redes neurais: quantização e poda. Existem muitas outras técnicas, portanto, sinta-se a vontade para assistir outras aulas do [curso MIT](https://hanlab.mit.edu/courses/2026-fall-65940). Porém, considero as três abaixo importantes para mostrar o que podemos fazer.

1. [Métricas de eficiência - vídeo-aula MIT](https://www.youtube.com/watch?v=CzGTQseaM38). Foco na segunda metade, a partir da parte "Efficiency Metrics".

2. [Quantização - vídeoaula MIT](https://www.youtube.com/watch?v=Qg_3N8pdK9s). Dê foco maior para a primeira metade da aula para uma ideia geral, mas sinta-se a vontade para ver o resto.

3. [Pruning/Poda - videoaula MIT](https://www.youtube.com/watch?v=47nNIPj3B98)