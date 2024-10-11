## Passo 1: Criar um Projeto de Biblioteca de Classes
	Crie um novo projeto e selecione "Biblioteca de Classes .NET Standard" ou "Biblioteca de Classes .NET Core", dependendo da sua necessidade1
## Passo 2: Adicionar Classes Reutiliz�veis

## Passo 3: Configurar Propriedades do Pacote
	* 1- Clique com o bot�o direito no projeto MinhaBiblioteca e selecione "Propriedades".
	* 2- Na aba "Package", preencha os detalhes do pacote, como nome, descri��o, vers�o, etc
## Passo 4: Gerar o Pacote NuGet
	No menu do Visual Studio, v� para Build > Pack
	Isso gerar� um arquivo .nupkg na pasta bin/Debug ou bin/Release do seu projeto.
## Passo 5: Publicar o Pacote NuGet
	Crie uma conta no NuGet.org, se ainda n�o tiver uma
	No Visual Studio, v� para Tools > NuGet Package Manager > Manage NuGet Packages for Solution
	Clique em Package Source e adicione o NuGet.org como uma fonte de pacotes
	Clique em Publish e siga as instru��es para fazer upload do seu pacote .nupkg para o NuGet.org
## Passo 6: Usar o Pacote em Outro Projeto
	Em outro projeto, v� para Tools > NuGet Package Manager > Manage NuGet Packages for Solution.

	Clique em Browse e procure por MinhaBiblioteca.

	Instale o pacote e use as classes reutiliz�veis no seu projeto.

	' using MinhaBiblioteca;

		class Program
		{
			static void Main(string[] args)
			{
				var calculadora = new Calculadora();
				Console.WriteLine($"Soma: {calculadora.Somar(10, 5)}");
				Console.WriteLine($"Subtra��o: {calculadora.Subtrair(10, 5)}");
				Console.WriteLine($"Multiplica��o: {calculadora.Multiplicar(10, 5)}");
				Console.WriteLine($"Divis�o: {calculadora.Dividir(10, 5)}");
			}
		}
	'
## Refer�ncias
	1 - https://learn.microsoft.com/pt-br/nuget/quickstart/create-and-publish-a-package-using-visual-studio?tabs=netcore-cli
	2 - https://learn.microsoft.com/pt-br/nuget/create-packages/package-authoring-best-practices
	