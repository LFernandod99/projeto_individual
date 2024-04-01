candidatos = [
    ["Candidato 1", "e5_t10_p8_s8"],
    ["Candidato 2", "e10_t7_p7_s8"],
    ["Candidato 3", "e8_t5_p4_s9"],
    ["Candidato 4", "e2_t2_p2_s1"],
    ["Candidato 5", "e10_t10_p8_s9"]
]

print(f'''{len(candidatos)} candidatos concorrem a esta vaga! Diga a media para cada hailidade''')

#Função para armazenar cada candidato
def buscar_candidatos(candidatos, entrevista, teorico, pratico, soft):
    candidatos_compativeis = []
