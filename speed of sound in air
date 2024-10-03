% Calculo velocidade do som no ar

clc; clear; format long

T_C = -100:1:400;   % vetor temperatura em graus Celsius
T_K = T_C + 273.15; % temperatura em Kelvin

gamma = 1.4; % coeficiente Poisson da Relacao de Mayer
R = 287; % constante dos gases ideais (para o ar) [J/kg*K]

c = sqrt(gamma*R*T_K); % velocidade do som em parametros de R e T [mts/seg]

c_aprox = (331.3 + 0.606*T_C); % velocidade do som linearizada

erro = 100*abs(c_aprox - c) ./ c; % erro percentual

figure;
title('Velocidade do Som no ar em Função da Temperatura');
plot(T_C, c, 'b', 'LineWidth', 2)
hold on;
plot(T_C, c_aprox, 'r--', 'LineWidth',2)
xlabel('Temperatura (°C)');
ylabel('Velocidade do som (m/s)');
legend('Ar como gás ideal', 'Expressão linearizada');

figure;
title('Erro percentual Linearizado em Função da Temperatura');
plot(T_C, erro, 'k', 'LineWidth',2)
xlabel('Temperatura (°C)');
ylabel('Erro (%)');
