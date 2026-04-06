# CTT09
Atividade para fluxo e exemplo da importância do CL

5. O Diagnóstico: Clique na execução que falhou. Vá até o passo “Rodar
Testes” e expanda o terminal. Responda (anote para discussão na aula):

## Qual foi a mensagem exata de erro que o Pytest imprimiu?
R: 
============================= test session starts ==============================
platform linux -- Python 3.11.15, pytest-9.0.2, pluggy-1.6.0
rootdir: /home/runner/work/CTT09/CTT09
plugins: anyio-4.13.0
collected 2 items

test_main.py .F                                                          [100%]

=================================== FAILURES ===================================
__________________________________ test_somar __________________________________

    def test_somar():
        response = client.get("/somar/5/3")
        assert response.status_code == 200
>       assert response.json() == {"resultado": 8}
E       AssertionError: assert {'resultado': 2} == {'resultado': 8}
E         
E         Differing items:
E         {'resultado': 2} != {'resultado': 8}
E         
E         Full diff:
E           {
E         -     'resultado': 8,
E         ?                  ^
E         +     'resultado': 2,
E         ?                  ^
E           }

test_main.py:14: AssertionError
=========================== short test summary info ============================
FAILED test_main.py::test_somar - AssertionError: assert {'resultado': 2} == {'resultado': 8}
  
  Differing items:
  {'resultado': 2} != {'resultado': 8}
  
  Full diff:
    {
  -     'resultado': 8,
  ?                  ^
  +     'resultado': 2,
  ?                  ^
    }
========================= 1 failed, 1 passed in 0.43s ==========================

## O que ele esperava receber e o que ele recebeu de fato?

R: ele estava esperando o valor 8, porém ao executar com o operador invertido ele retorna 2, resultando na diferença esperada para o status 200.