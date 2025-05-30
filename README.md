# Escola-Mongoose

C:\Users\Bruna>curl -X POST http://localhost:3000/professor -H "Content-Type: application/json" -d "{\"nome\": \"Henrique Louro\", \"email\": \"henrique.louro@fatec.sp.gov.br\",  \"cpf\": \"07494812857\"}"
{"nome":"Henrique Louro","email":"henrique.louro@fatec.sp.gov.br","cpf":"07494812857","_id":"6838fa1318bc4405f1a662e5","__v":0}
C:\Users\Bruna>curl -X POST http://localhost:3000/professor -H "Content-Type: application/json" -d "{\"nome\": \"Carlos Silva\", \"email\": \"carlos.silva@fatec.sp.gov.br\",  \"cpf\": \" 63479695051\"}"
{"nome":"Carlos Silva","email":"carlos.silva@fatec.sp.gov.br","cpf":"63479695051","_id":"6838fa5918bc4405f1a662e7","__v":0}
C:\Users\Bruna>curl -X POST http://localhost:3000/professor -H "Content-Type: application/json" -d "{\"nome\": \"Odete Roitman\", \"email\": \"odete.roitman@fatec.sp.gov.br\",  \"cpf\": \" 32082128016\"}"
{"nome":"Odete Roitman","email":"odete.roitman@fatec.sp.gov.br","cpf":"32082128016","_id":"6838fa6d18bc4405f1a662e9","__v":0}
C:\Users\Bruna>curl -X POST http://localhost:3000/professor -H "Content-Type: application/json" -d "{\"nome\": \"Henrique Louro\", \"email\": \"henrique.louro@fatec.sp.gov.br\",  \"cpf\": \"07494812857\"}"
{"message":"CPF ou e-Mail já em uso"}
C:\Users\Bruna>curl -X POST http://localhost:3000/professor -H "Content-Type: application/json" -d "{\"nome\": \"Henrique Louro\", \"email\": \"henrique.louro@fatec.sp.gov.br\",  \"cpf\": \"12345678910\"}"
{"message":"12345678910 não é um CPF válido"}
C:\Users\Bruna>curl -X POST http://localhost:3000/professor -H "Content-Type: application/json" -d "{\"nome\": \"Henrique Louro\", \"email\": \"henrique.louro@fatec\",  \"cpf\": \"12345678910\"}"
{"message":"henrique.louro@fatec não é um formato de e-mail válido"}
C:\Users\Bruna>curl -X GET http://localhost:3000/professor
[{"_id":"6838fa1318bc4405f1a662e5","nome":"Henrique Louro","email":"henrique.louro@fatec.sp.gov.br","cpf":"07494812857","__v":0},{"_id":"6838fa5918bc4405f1a662e7","nome":"Carlos Silva","email":"carlos.silva@fatec.sp.gov.br","cpf":"63479695051","__v":0},{"_id":"6838fa6d18bc4405f1a662e9","nome":"Odete Roitman","email":"odete.roitman@fatec.sp.gov.br","cpf":"32082128016","__v":0}]
C:\Users\Bruna>curl -X PUT http://localhost:3000/professor -H "Content-Type: application/json" -d "{\"id\":\"6838fa6d18bc4405f1a662e9\",\"nome\": \"Odetinha Roitman\", \"email\": \"odetinha.roitman@fatec.sp.gov.br\",  \"cpf\": \" 32082128016\"}"
{"_id":"6838fa6d18bc4405f1a662e9","nome":"Odetinha Roitman","email":"odetinha.roitman@fatec.sp.gov.br","cpf":"32082128016","__v":0}
C:\Users\Bruna>curl -X DELETE http://localhost:3000/professor -H "Content-Type: application/json" -d "{\"id\":\"6838fa6d18bc4405f1a662e9\"}"
{"message":"Professor excluído com sucesso"}
C:\Users\Bruna>curl -X GET http://localhost:3000/professor
[{"_id":"6838fa1318bc4405f1a662e5","nome":"Henrique Louro","email":"henrique.louro@fatec.sp.gov.br","cpf":"07494812857","__v":0},{"_id":"6838fa5918bc4405f1a662e7","nome":"Carlos Silva","email":"carlos.silva@fatec.sp.gov.br","cpf":"63479695051","__v":0}]
C:\Users\Bruna>curl -X POST http://localhost:3000/disciplina -H "Content-Type: application/json" -d "{\"descricao\": \"Técnicas de Programação II\"}"
{"descricao":"Técnicas de Programação II","_id":"6838fbf418bc4405f1a662f4","__v":0}
C:\Users\Bruna>curl -X POST http://localhost:3000/disciplina -H "Content-Type: application/json" -d "{\"descricao\": \"Lógica de Programação\"}"
{"descricao":"Lógica de Programação","_id":"6838fc0d18bc4405f1a662f6","__v":0}
C:\Users\Bruna>curl -X GET http://localhost:3000/disciplina
[{"_id":"6838fbf418bc4405f1a662f4","descricao":"Técnicas de Programação II","__v":0},{"_id":"6838fc0d18bc4405f1a662f6","descricao":"Lógica de Programação","__v":0}]
C:\Users\Bruna>curl -X POST http://localhost:3000/professor_has_disciplina -H "Content-Type: application/json" -d "{\"professor\": \"6838fa1318bc4405f1a662e5\", \"disciplina\": \"6838fbf418bc4405f1a662f4\"}"
{"professor":"6838fa1318bc4405f1a662e5","disciplina":"6838fbf418bc4405f1a662f4","_id":"6838fc5618bc4405f1a662f9","__v":0}
C:\Users\Bruna>curl -X POST http://localhost:3000/professor_has_disciplina -H "Content-Type: application/json" -d "{\"professor\": \"6838fa5918bc4405f1a662e7\", \"disciplina\": \"6838fc0d18bc4405f1a662f6\"}"
{"professor":"6838fa5918bc4405f1a662e7","disciplina":"6838fc0d18bc4405f1a662f6","_id":"6838fc7c18bc4405f1a662fd","__v":0}
C:\Users\Bruna>
