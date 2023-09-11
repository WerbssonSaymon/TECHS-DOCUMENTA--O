Jest é um framework de testes em javascript

Instalação do Jest via npm 
npm install --save-dev jest

Pasta padrão para guardar os testes
__TESTS__

Extensões
.spec.js
.test.js

O Jest usa "matchers" para que você possa testar valores de maneiras diferentes

Estrutura de teste simples

test('mensagem sobre o que é o teste', () => {
  expect().toBe();
});
expect é a expectativa e depois dela matcher que espera o resultado esperado

test('dois mais dois é quatro', () => {
  expect(2 + 2).toBe(4);
});