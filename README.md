# CALCULO-DE-VENDAS-CODIGO-JAVA
Elabore um programa que preencha uma matriz 12 x 4 com os valores das vendas de uma loja, em que cada linha representa um mês do ano e cada coluna representa uma semana do mês. O programa deverá calcular e mostrar:

o total vendido em cada mês do ano, mostrando o nome do mês por extenso;
o total vendido pela loja no ano.
Complete o programa abaixo, arrastando e soltando os trechos de código nos espaços em branco, de forma que o problema acima seja corretamente implementado.

public class TotalVendas {
	public static void main(String[] args) {
		double[][] vendas = new double[12][4];
		String[] meses = {"Janeiro", "Fevereiro", "Marco", "Abril", "Maio", "Junho", 
		                  "Julho", "Agosto", "Setembro", "Outubro", "Novembro", "Dezembro"};
		
		for(int mes = 0; mes < vendas.length; mes++) { 
			for(int semana = 0; semana < vendas[mes].length; semana++) {
				System.out.printf("Vendas na semana %d em %s: ", semana+1, meses[mes]);
				vendas[mes][semana] = Double.parseDouble(System.console().readLine());
			}
		}
		
		System.out.println("\n-------------------- VENDAS POR MES --------------------");
		[double totalAno = 0;]
		[for(int mes = 0; mes < vendas.length; mes++)] { 
			double totalMes = 0;
			[for(int semana = 0; semana < vendas[mes].length; semana++)] {
				[totalMes += vendas[mes][semana];]
			}
			[System.out.printf("%s = R$ %.2f\n", meses[mes], totalMes);]
			[totalAno += totalMes;]
		}
		[System.out.printf("\nTOTAL DE VENDAS NO ANO = R$ %.2f\n", totalAno);]
	}
}


