Projetinho de gerenciamento de pacientes hospitalares

Introdução 

Este documento descreve os requisitos e casos de uso da tela de cadastro e visualização de pacientes em um sistema. A tela de cadastro deve permitir o cadastro de um novo paciente com informações obrigatórias, validar o preenchimento correto dessas informações e permitir a associação de um convênio já cadastrado no sistema. Já a tela de visualização deve permitir a visualização dos dados dos pacientes cadastrados, preencher automaticamente a tabela ao abrir a janela, permitir a filtragem por ID, CPF ou nome do paciente e a limpeza do filtro aplicado para exibir todos os pacientes cadastrados. O documento apresenta os requisitos funcionais, as regras de negócio e os casos de uso relacionados a essas telas. 

 

Requisitos da tela de cadastro do cliente 

 

Requisitos funcionais – Cadastro do cliente 

[RF01] O sistema deve permitir o cadastro de um novo paciente no sistema, com as seguintes informações obrigatórias: nome completo, CPF, data de nascimento, endereço e telefone. 

[RF02] O sistema deve permitir verificar se os campos obrigatórios foram preenchidos corretamente antes de permitir o cadastro do paciente. 

[RF03] O sistema deve permitir a seleção de um convênio cadastrado no sistema para associar ao paciente. 

 

Regras de negócio – Cadastro do cliente 

[RN01]: Nome: campo obrigatório com no máximo 55 caracteres 

[RN02]: CPF: campo obrigatório contendo 11 caracteres e sendo único no sistema. 

[RN03]: Data de nascimento: campo obrigatório; deve ser uma data válida (DD/MM/AAAA) 

[RN04]: Endereço: campo obrigatório com no máximo 200 caracteres 

[RN05]: Telefone: campo obrigatório com no máximo 15 caracteres com formato (xx)xxxx-xxxx 

[RN06]: E-mail: campo opcional; deve ser válido 

[RN07]: Convênio: campo obrigatório; deve estar cadastrado no sistema 

 

Casos de uso – Cadastro do cliente 

 

UC1 – Cadastro de novo paciente 

Número do requisito: RF01 

Ator principal: atendente  

Pré-condições: atendente tem acesso ao sistema. 

Fluxo principal: 

Atendente seleciona a opção de cadastrar novo paciente. 

Sistema exibe tela de cadastro de paciente com os campos obrigatórios a serem preenchidos. 

Atendente preenche os campos obrigatórios com as informações do novo paciente. 

Atendente salva o cadastro do novo paciente. 

Sistema exibe mensagem de confirmação do cadastro realizado com sucesso. 

Pós-condições: cadastro do novo paciente é salvo no sistema com sucesso. 

 

UC2 – Verificação dos campos obrigatórios 

Número do requisito: RF02  

Ator principal: sistema  

Pré-condições: atendente tem acesso ao sistema. 

Fluxo principal: 

Atendente seleciona a opção de cadastrar. 

Sistema exibe tela de cadastro de paciente com os campos obrigatórios a serem preenchidos. 

Atendente preenche todos os campos, incluindo os obrigatórios. 

Atendente solicita ação de salvar o cadastro/edição. 

Sistema verifica se todos os campos obrigatórios foram preenchidos corretamente. 

Caso algum campo obrigatório não tenha sido preenchido corretamente, o sistema exibe mensagem de erro e impede a realização da ação solicitada. 

Caso todos os campos obrigatórios tenham sido preenchidos corretamente, o sistema realiza a ação solicitada (salvar cadastro). 

Pós-condições: cadastro do paciente é salvo no sistema com sucesso apenas se todos os campos obrigatórios foram preenchidos corretamente. 

 

UC3 – Seleção de convênio para associar ao paciente 

Número do requisito: RF03  

Ator principal: atendente  

Pré-condições: atendente tem acesso ao sistema e convênio já está cadastrado no sistema. 

Fluxo principal: 

Atendente seleciona a opção de cadastrar paciente. 

Sistema exibe tela de cadastro de paciente. 

Atendente seleciona a opção de associar convênio ao paciente. 

Sistema exibe lista de convênios cadastrados no sistema. 

Atendente seleciona o convênio desejado. 

Sistema associa o convênio selecionado ao paciente. 

Atendente salva o cadastro do paciente. 

Sistema exibe mensagem de confirmação do cadastro realizado com sucesso. 

Pós-condições: convênio é associado ao paciente no cadastro e o paciente é salvo no sistema com sucesso. 

 

 

 

 

 

 

 

 

 

Requisitos da tela de visualização de pacientes 

 

Requisitos funcionais – Visualização de pacientes 

 

[RF01]: O sistema deve permitir a visualização dos dados dos pacientes cadastrados no sistema. 

[RF02]: O sistema deve ser preenchido automaticamente com os dados dos pacientes cadastrados no sistema ao abrir a janela. 

[RF03]: O sistema deve permitir filtrar a tabela por ID, CPF ou nome do paciente. 

[RF04]: O sistema deve permitir a limpeza do filtro aplicado e a exibição de todos os pacientes cadastrados no sistema. 

 

Regras de negócio – Visualização de pacientes 

 

[RN01]: A tela de visualização do cliente deve ser preenchida automaticamente com os dados dos pacientes cadastrados no sistema ao ser aberta. 

[RN02]: Os campos de filtro por ID, CPF ou nome do paciente devem ser validados para garantir que o usuário inseriu apenas caracteres numéricos no caso do ID, e caracteres alfabéticos no caso do nome do paciente e do CPF. 

[RN03]: A filtragem da tabela deve ser realizada somente com os dados dos pacientes cadastrados no sistema. 

 

Casos de uso – Cadastro do cliente 

 

UC1 – Visualização de pacientes 

Número do requisito: RF01 

Ator principal: atendente 

Pré-condições: atendente tem acesso ao sistema. 

Fluxo principal: 

Atendente seleciona a opção de visualização de pacientes. 

Sistema exibe a lista de todos os pacientes cadastrados no sistema, com seus respectivos dados. 

Pós-condições: nenhuma 

 

UC2 – Preenchimento automático dos dados dos pacientes ao abrir a janela 

Número do requisito: RF02 

Ator principal: sistema 

Pré-condições: nenhuma 

Fluxo principal: 

Sistema abre a janela de visualização de pacientes. 

Sistema busca os dados de todos os pacientes cadastrados no sistema. 

Sistema preenche automaticamente os campos da tabela de visualização de pacientes com os dados dos pacientes cadastrados. 

Pós-condições: nenhuma 

 

UC3 – Filtragem de pacientes por ID, CPF ou nome 

Número do requisito: RF03 

Ator principal: atendente 

Pré-condições: atendente tem acesso ao sistema 

Fluxo principal: 

Atendente seleciona a opção de filtragem de pacientes por ID, CPF ou nome. 

Sistema exibe os campos de filtro na tela de visualização de pacientes. 

Atendente preenche um ou mais campos de filtro com os valores desejados. 

Sistema realiza a filtragem da tabela de pacientes de acordo com os valores inseridos nos campos de filtro. 

Pós-condições: nenhuma 

 

UC4 – Limpeza do filtro e exibição de todos os pacientes 

Número do requisito: RF04 

Ator principal: atendente 

Pré-condições: atendente tem acesso ao sistema e um filtro de pacientes está aplicado. 

Fluxo principal: 

Atendente seleciona a opção de limpar o filtro. 

Sistema remove o filtro anteriormente aplicado na tabela de pacientes e exibe todos os pacientes cadastrados no sistema. 

Pós-condições: nenhuma 
