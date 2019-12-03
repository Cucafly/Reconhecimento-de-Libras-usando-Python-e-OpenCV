# Reconhecimento-de-Libras-usando-Python-e-OpenCV

# Instruções
# As linhas de codigo abaixo deverão ser executadas no Google Colab. Primeiro salve os arquivos no seu Google Drive. Depois, crie um diretório. Obs.: os "paths" deverão ser os mesmos criados e não os indicados nas linhas de código abaixo.

Mão - Traduzindo Libras em imagens

Para a identificação mais dinâmica de várias posições, foram desenvolvidos 4 módulos para extrair algumas caracteríscas e comparar o deslocamento das articulações (pontos chave)

Extraimos a ALTURA, POSIÇÃO e PROXIMIDADE entre os pontos chave detectados

Módulo extrator_ALTURA: verifica se um ponto está 'acima' ou 'abaixo' de outro ponto específico. Por exemplo, se a ponta do dedo está 'acima' do punho     

Módulo extrator_POSICAO: funções para verificar se os dedos estão 'dobrados' ou 'esticados', na posição horizontal ou na vertical. Também recebe o resultado do módulo extrator_ALTURA para saber em que posição a mão está (voltada 'acima' ou 'abaixo')         

Módulo extrator_PROXIMIDADE: funções que comparam a proximidade entre os pontos chaves detectados. Por exemplo, se o resultado do módulo extrator_POSICAO for igual a 'dobrado' para o dedo indicador e dedo médio e ambos estiverem na mesma altura, então significa que os dedos estão próximos         

Módulo alfabeto: após extrair todas estas características, foi criado o alfabeto de características, onde um VETOR DE VETORES recebe o resultado de todos os módulos extratores. Assim usamos este módulo para comparar com uma nova análise (nova imagem) de entrada              

Não foram usadas as letras: H, J, K, X, ,Y , Z devido ao movimento adicional para a execução correta das letras.             

Estas letras podem ser analisadas em uma função diferente, semelhante a função de análise de posicionamento do corpo, onde comparamos a transição entre pontos              

Letra T: para o dedo polegar, devido a estar sobreposto pelo dedo indicador, o algoritmo não reconhece os pontos da ponta do dedo. Letra N e U se confundem

Obs.: o algoritmo ainda está sendo aperfeiçoado.
