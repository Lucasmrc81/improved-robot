using System;
using System.Collections.Generic;

class Program
{
    static List<PC> pcsOnline = new List<PC>();

    static void Main()
    {
        while (true)
        {
            Console.WriteLine("\nEscolha uma opção:");
            Console.WriteLine("1. Listar PCs Online");
            Console.WriteLine("2. Adicionar PC Online");
            Console.WriteLine("3. Configurar PC Remoto");
            Console.WriteLine("4. Monitorar PC Remoto");
            Console.WriteLine("0. Sair");

            string escolha = Console.ReadLine();

            switch (escolha)
            {
                case "1":
                    ListarPCsOnline();
                    break;

                case "2":
                    AdicionarPCOnline();
                    break;

                case "3":
                    Console.WriteLine("Informe o nome do PC a ser configurado:");
                    string nomePC = Console.ReadLine();
                    ConfigurarPCRemoto(nomePC);
                    break;

                case "4":
                    Console.WriteLine("Informe o nome do PC a ser monitorado:");
                    nomePC = Console.ReadLine();
                    MonitorarPCRemoto(nomePC);
                    break;

                case "0":
                    Console.WriteLine("Saindo do programa. Até logo!");
                    Environment.Exit(0);
                    break;

                default:
                    Console.WriteLine("Opção inválida. Tente novamente.");
                    break;
            }
        }
    }

    static void ListarPCsOnline()
    {
        Console.WriteLine("\nPCs Online:");
        foreach (var pc in pcsOnline)
        {
            Console.WriteLine($"{pc.Nome} - {pc.EnderecoIP}");
        }
    }

    static void AdicionarPCOnline()
    {
        Console.WriteLine("Informe o nome do novo PC:");
        string nomePC = Console.ReadLine();
        Console.WriteLine("Informe o endereço IP do novo PC:");
        string enderecoIP = Console.ReadLine();

        pcsOnline.Add(new PC { Nome = nomePC, EnderecoIP = enderecoIP });

        Console.WriteLine($"PC {nomePC} adicionado com sucesso!");
    }

    static void ConfigurarPCRemoto(string nome)
    {
        PC pcSelecionado = pcsOnline.Find(pc => pc.Nome == nome);
        if (pcSelecionado != null)
        {
            Console.WriteLine($"Configurando o PC {pcSelecionado.Nome} ({pcSelecionado.EnderecoIP})...");
            // Adicione lógica de configuração aqui
        }
        else
        {
            Console.WriteLine($"PC com o nome {nome} não encontrado.");
        }
    }

    static void MonitorarPCRemoto(string nome)
    {
        PC pcSelecionado = pcsOnline.Find(pc => pc.Nome == nome);
        if (pcSelecionado != null)
        {
            Console.WriteLine($"Monitorando o PC {pcSelecionado.Nome} ({pcSelecionado.EnderecoIP})...");
            // Adicione lógica de monitoramento aqui
        }
        else
        {
            Console.WriteLine($"PC com o nome {nome} não encontrado.");
        }
    }
}

class PC
{
    public string Nome { get; set; }
    public string EnderecoIP { get; set; }
}
