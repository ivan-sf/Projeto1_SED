# Controle de um Sistema de Robôs Autônomos em um Armazém

Este repositório é referente ao Projeto 01 da disciplina Sistemas a Eventos Discretos, no período 2024.2, pela Universidade Federal de Campina Grande (UFCG).

---

## Equipe
- Arthur de Queiroz Tavares Borges Mesquita (120110246)
- Ivan da Silva Filho (120110348)
- Jayne Emilly Silva de Melo (121210548)

---

## Descrição

Este é um projeto para implementação de um armazém automatizado. Neste sentido, dois robôs móveis transportam caixas de insumos entre um Buffer de Entrada (BE) e máquinas de processamento, cada um possuindo uma rota específica, podendo ocorrer eventos de 
solicitação, descarga e falhar. 
Caso um dos robôs falhe em algum momento, este irá ter como evento futuro o conserto e, enquanto esse não ocorrer, um terceiro robô irá substituí-lo.
Será utilizado o software Supremica para a implementação dos autômatos.

---

## Objetivos

1. Modelar o comportamento dos robôs por meio de autômatos finitos;
2. Definir estados e transições para a movimentação das caixas entre o BE e as máquinas;
3. Garantir que o robô tenha acesso ao BE antes de iniciar o transporte;
4. Implementar a especificação e gerar o supervisor correspondente;
5. Representar as restrições de segurança utilizando autômatos de especificação;
6. Utilizar o Supremica para a síntese do supervisor;
7. Simular e validar o funcionamento do sistema;
8. Testar diferentes cenários de transporte para verificar a segurança do supervisor;
9. Analisar o desempenho do sistema.

---

## Funcionalidades
- Controle de robôs para carga e descarga das caixas de insumos
- Substituição temporária de um robô em caso de falha

---

## Modelagem

O sistema em questão faz uso de autômatos finitos, que são os robôs, o controle destes, as máquinas e o supervisor. 

### Eventos controláveis
- `move(Rx, BE, My)`: robô **Rx** transporta uma caixa de insumos do buffer **BE** para a máquina **My**;
- `unload(Rx, My)`: robô **Rx** faz o descarregamento da caixa de insumos na máquina **My**.

### Eventos não controláveis
- `req(BE, My)`: solicitação de transporte da máquina **My**;
- `broken(Rx)`: robô Rx apresenta falha;
- `repair(Rx)`: robô Rx é reparado e volta a operar.

### Autômatos 

- Autômatos dos robôs R1 e R2
<div align="center">
  <img src="https://github.com/user-attachments/assets/5b0e507c-01b5-4d9c-bd5e-180928dd2f2a" alt="R1" style="width:30%;"/> <img src="https://github.com/user-attachments/assets/cb6abce3-5da4-4346-86a0-14cc97f9b70e" alt="R2" style="width:29%;"/>
</div>

- Autômatos das máquinas M1, M2, M3 e M4
<div align="center">
  <img src="https://github.com/user-attachments/assets/8c89ca3c-51c8-4913-8485-020dc5eb9492" alt="M1" style="width:30%;"/> <img src="https://github.com/user-attachments/assets/c72ce7cb-54a5-485f-97bf-84b0656f7c2d" alt="M2" style="width:27%;"/>
</div>

<div align="center">
  <img src="https://github.com/user-attachments/assets/e962e1b7-576c-44ec-98bd-5c4717bcd4ce" alt="M3" style="width:30%;"/> <img src="https://github.com/user-attachments/assets/2c33f56e-f8e2-45de-a6d8-87a8a714d8c7" alt="M4" style="width:28%;"/>
</div>

- Autômato do robô R3
<div align="center">
  <img src="https://github.com/user-attachments/assets/71641097-92ac-462f-8e34-19f139752a68" alt="R3" style="width:30%;"/>
</div>

- Autômatos de controle dos robôs R1 e R2
<div align="center">
  <img src="https://github.com/user-attachments/assets/d30138cc-90c0-43a4-9497-db540d853db6" alt="C_R1" style="width:28%;"/> <img src="https://github.com/user-attachments/assets/b0808f66-cb97-4537-a5ea-11e8afb55a29" alt="C_R2" style="width:30%;"/>
</div>

---

## Vídeo de apresentação
Link de acesso ao vídeo no YouTube do ArthurzinhoGameplays2002: 
