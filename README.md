candidatos = [
    ["Candidato 1", "e5_t10_p8_s8"],
    ["Candidato 2", "e10_t7_p7_s8"],
    ["Candidato 3", "e8_t5_p4_s9"],
    ["Candidato 4", "e2_t2_p2_s1"],
    ["Candidato 5", "e10_t10_p8_s9"]  
]
print(f'''{len(candidatos)} candidatos concorrem a esta vaga! Diga a media para cada hailidade''')

entrevista = float(input("Digite a nota mínima para a entrevista: "))
teorico = float(input("Digite a nota mínima para o teste teórico: "))
pratico = float(input("Digite a nota mínima para o teste prático: "))
soft = float(input("Digite a nota mínima para a avaliação de soft skills: "))

def buscar_candidatos(candidatos, entrevista, teorico, pratico, soft):
      candidatos_compativeis = []
      for candidato in candidatos:
            notas = [float(nota[1:]) 
                 for nota in candidato[1].split('_')]
            if notas[0] >= entrevista and notas[1] >= teorico and notas[2] >= pratico and notas[3] >= soft: candidatos_compativeis.append(candidato[0])
            return candidatos_compativeis
      

candidatos_compativeis = buscar_candidatos(candidatos, entrevista, teorico, pratico, soft)

if candidatos_compativeis:
    print("Candidatos compatíveis com os critérios escolhidos:")
    for candidato in candidatos_compativeis:
        print(candidato)
else:
    print("Nenhum candidato encontrado com os critérios compativeis.")
