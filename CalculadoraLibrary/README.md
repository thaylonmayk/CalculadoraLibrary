## Passo 1: Criar um Projeto de Biblioteca de Classes
	Crie um novo projeto e selecione "Biblioteca de Classes .NET Standard" ou "Biblioteca de Classes .NET Core", dependendo da sua necessidade1
## Passo 2: Adicionar Classes Reutilizáveis

## Passo 3: Configurar Propriedades do Pacote
	* 1- Clique com o botão direito no projeto MinhaBiblioteca e selecione "Propriedades".
	* 2- Na aba "Package", preencha os detalhes do pacote, como nome, descrição, versão, etc
## Passo 4: Gerar o Pacote NuGet
	No menu do Visual Studio, vá para Build > Pack
	Isso gerará um arquivo .nupkg na pasta bin/Debug ou bin/Release do seu projeto.
## Passo 5: Publicar o Pacote NuGet
	Crie uma conta no NuGet.org, se ainda não tiver uma
	No Visual Studio, vá para Tools > NuGet Package Manager > Manage NuGet Packages for Solution
	Clique em Package Source e adicione o NuGet.org como uma fonte de pacotes
	Clique em Publish e siga as instruções para fazer upload do seu pacote .nupkg para o NuGet.org
## Passo 6: Usar o Pacote em Outro Projeto
	Em outro projeto, vá para Tools > NuGet Package Manager > Manage NuGet Packages for Solution.

	Clique em Browse e procure por MinhaBiblioteca.

	Instale o pacote e use as classes reutilizáveis no seu projeto.

	' using MinhaBiblioteca;

		class Program
		{
			static void Main(string[] args)
			{
				var calculadora = new Calculadora();
				Console.WriteLine($"Soma: {calculadora.Somar(10, 5)}");
				Console.WriteLine($"Subtração: {calculadora.Subtrair(10, 5)}");
				Console.WriteLine($"Multiplicação: {calculadora.Multiplicar(10, 5)}");
				Console.WriteLine($"Divisão: {calculadora.Dividir(10, 5)}");
			}
		}
	'
## Referências
	1 - https://learn.microsoft.com/pt-br/nuget/quickstart/create-and-publish-a-package-using-visual-studio?tabs=netcore-cli
	2 - https://learn.microsoft.com/pt-br/nuget/create-packages/package-authoring-best-practices
	