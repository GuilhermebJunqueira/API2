# API2


package org.example;

import javax.swing.*;
import java.awt.*;
import java.awt.event.ActionEvent;
import java.awt.event.ActionListener;

public class InformacoesClimaticas extends JFrame {
    private JLabel labelUmidade, labelPressao, labelChuva, labelTemperatura, labelPtoOrvalho,
            labelRadiacao, labelVelVento, labelRajVento, labelInsolacao, labelNebulosidade;
    private JTextField campoUmidadeMin, campoUmidadeMax, campoPressaoMin, campoPressaoMax, campoChuvaMin, campoChuvaMax,
            campoTemperaturaMin, campoTemperaturaMax, campoPtoOrvalhoMin, campoPtoOrvalhoMax,
            campoRadiacaoMin, campoRadiacaoMax, campoVelVentoMin, campoVelVentoMax,
            campoRajVentoMin, campoRajVentoMax, campoInsolacaoMin, campoInsolacaoMax,
            campoNebulosidadeMin, campoNebulosidadeMax;
    private JButton buttonCalcular;

    public InformacoesClimaticas() {
        setTitle("Informações Climáticas");
        setSize(600, 400);
        setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);

        initComponents();
        setLayout(new GridLayout(12, 3)); // Ajustado para acomodar os rótulos de Mínimo e Máximo

        // Adiciona os rótulos de "Mínimo" e "Máximo" no topo
        add(new JLabel(""));
        add(new JLabel("Mínimo"));
        add(new JLabel("Máximo"));

        // Adiciona os campos para cada tipo de informação
        add(labelUmidade);
        add(campoUmidadeMin);
        add(campoUmidadeMax);

        add(labelPressao);
        add(campoPressaoMin);
        add(campoPressaoMax);

        add(labelChuva);
        add(campoChuvaMin);
        add(campoChuvaMax);

        add(labelTemperatura);
        add(campoTemperaturaMin);
        add(campoTemperaturaMax);

        add(labelPtoOrvalho);
        add(campoPtoOrvalhoMin);
        add(campoPtoOrvalhoMax);

        add(labelRadiacao);
        add(campoRadiacaoMin);
        add(campoRadiacaoMax);

        add(labelVelVento);
        add(campoVelVentoMin);
        add(campoVelVentoMax);

        add(labelRajVento);
        add(campoRajVentoMin);
        add(campoRajVentoMax);

        add(labelInsolacao);
        add(campoInsolacaoMin);
        add(campoInsolacaoMax);

        add(labelNebulosidade);
        add(campoNebulosidadeMin);
        add(campoNebulosidadeMax);

        // Adiciona o botão calcular em uma linha separada
        add(new JLabel(""));
        add(buttonCalcular);

        setVisible(true);
    }

    private void initComponents() {
        labelUmidade = new JLabel("Umidade:");
        campoUmidadeMin = new JTextField();
        campoUmidadeMax = new JTextField();

        labelPressao = new JLabel("Pressão:");
        campoPressaoMin = new JTextField();
        campoPressaoMax = new JTextField();

        labelChuva = new JLabel("Chuva:");
        campoChuvaMin = new JTextField();
        campoChuvaMax = new JTextField();

        labelTemperatura = new JLabel("Temperatura:");
        campoTemperaturaMin = new JTextField();
        campoTemperaturaMax = new JTextField();

        labelPtoOrvalho = new JLabel("Ponto de Orvalho:");
        campoPtoOrvalhoMin = new JTextField();
        campoPtoOrvalhoMax = new JTextField();

        labelRadiacao = new JLabel("Radiação:");
        campoRadiacaoMin = new JTextField();
        campoRadiacaoMax = new JTextField();

        labelVelVento = new JLabel("Velocidade do Vento:");
        campoVelVentoMin = new JTextField();
        campoVelVentoMax = new JTextField();

        labelRajVento = new JLabel("Rajada de Vento:");
        campoRajVentoMin = new JTextField();
        campoRajVentoMax = new JTextField();

        labelInsolacao = new JLabel("Insolação:");
        campoInsolacaoMin = new JTextField();
        campoInsolacaoMax = new JTextField();

        labelNebulosidade = new JLabel("Nebulosidade:");
        campoNebulosidadeMin = new JTextField();
        campoNebulosidadeMax = new JTextField();

        buttonCalcular = new JButton("Calcular");
        buttonCalcular.addActionListener(new ActionListener() {
            @Override
            public void actionPerformed(ActionEvent e) {
                calcularMinMax();
            }
        });
    }

    private void calcularMinMax() {
        // Aqui você pode implementar a lógica para calcular o máximo e o mínimo de cada campo
        // Usando os valores dos campos de texto
        // Por exemplo, pode percorrer todos os campos e calcular os valores máximos e mínimos
        // Depois, exibir esses valores em uma nova janela ou em um JOptionPane

        JOptionPane.showMessageDialog(this, "Cálculo de máximos e mínimos não implementado ainda.");
    }

    public static void main(String[] args) {
        SwingUtilities.invokeLater(new Runnable() {
            @Override
            public void run() {
                new InformacoesClimaticas();
            }
        });
    }
}
