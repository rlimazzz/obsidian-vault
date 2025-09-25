Site: https://dbis-uibk.github.io/relax/landing
Banco de Dados : PhotoDB

E se eu quiser fazer uma consulta que mostra o firstname, lastname, birthday, personId, salary e experience?
$temp = (employees) \bowtie employess.personId  , photographers.employeeId  (photographers)$$(persons) ⟕ persons.id = employees.personId (temp)$

E se eu quiser fazer uma consulta que mostre o employeeId, firstname e salary?

$fsalario = π employeeId, salary ((employees) ⨝ employees.personId = photographers.employeeId (photographers))$$π  employeeId, firstname, salary ((persons) ⨝ persons.id = fsalario.employeeId (fsalario))$
E se eu quiser saber quais pessoas não estão empregadas?
$empregados = π id, lastname, firstname, birthday((employees)⨝ employees.personId = persons.id (persons))$$π firstname, lastname(persons - empregados)$

ou 

$naoempregados = π id (π id (persons)- π personId (employees))$
$π id, firstname, lastname ((persons) ⨝ (naoempregados))$

E se eu quiser saber a quantidade de fotos que cada marca de câmera tirou?

$γ brand ; count(cameraId)→ qtd_fotos((photos) ⨝ cameraId = cameras.id (cameras))$
O operador γ serve como agrupamento,

