## Adicionar dados no arquivo JSON.
<ul><li>Criando a classe ArquivoJson.</li></ul>

<pre>
  <code>
public void AdicionarDados(string arquivo) {

}
  </code>
</pre>

<ul><li>Criando o método AdicionarDados que recebe um parâmetro string</li></ul>

<pre>
  <code>
public void AdicionarDados(string arquivo) {

}
  </code>
</pre>

<ul><li>Caminho do arquivo JSON</li></ul>

<pre>
  <code>
    string caminhoArquivoJson = arquivo;
  </code>
</pre>

<ul><li>Criar uma nova instância de Pessoa</li></ul>

<pre>
  <code>
Pessoa novaPessoa = new Pessoa();
  </code>
</pre>

<ul><li>Solicitar que o usuário insira os dados</li></ul>

<pre>
  <code>
Console.Write("Digite o nome: ");
novaPessoa.Nome = Console.ReadLine();
  </code>
</pre>

<ul><li>Conversão de string para int</li></ul>

<pre>
  <code>
Console.Write("Digite a idade: ");
novaPessoa.Idade = int.Parse(Console.ReadLine());
  </code>
</pre>

<ul><li>Criar uma nova instância de Endereco.</li></ul>

<pre>
  <code>
novaPessoa.Endereco = new Endereco();
  </code>
</pre>

<ul><li>Solicitar que o usuário insira os dados.</li></ul>

<pre>
  <code>
Console.Write("Digite a rua: ");
novaPessoa.Endereco.Rua = Console.ReadLine();

Console.Write("Digite a cidade: ");
novaPessoa.Endereco.Cidade = Console.ReadLine();
  </code>
</pre>

<ul><li>Ler o JSON existente do arquivo.</li></ul>

<pre>
  <code>
List<Pessoa> listaPessoas = new List<Pessoa>();
  </code>
</pre>

<ul><li>Verifica se o arquivo JSON existe e se seu tamanho é maior que 0 bytes</li></ul>

<pre>
  <code>
if (File.Exists(caminhoArquivoJson) && new FileInfo(caminhoArquivoJson).Length &#62 0) {
    
    // Se o arquivo existe e não está vazio, lê o conteúdo do arquivo JSON para uma string
    string jsonExistente = File.ReadAllText(caminhoArquivoJson);

    // Desserializa a string JSON lida para uma lista de objetos do tipo Pessoa
    listaPessoas = JsonConvert.DeserializeObject&#60List&#60Pessoa&#62&#62(jsonExistente);
      
} else {

      // Se o arquivo não existir ou estiver vazio, inicializa uma nova lista de objetos do tipo Pessoa
    listaPessoas = new List&#60Pessoa&#62();

}
  </code>
</pre>

<ul><li>novaPessoa adicionada na listaPessoa.</li></ul>

<pre>
  <code>
listaPessoas.Add(novaPessoa);
  </code>
</pre>

<ul><li>Serializar a lista atualizada de volta para JSON.</li></ul>

<pre>
  <code>
string jsonAtualizado = JsonConvert.SerializeObject(listaPessoas, Formatting.Indented);
  </code>
</pre>

<ul><li>Escrever o JSON atualizado de volta para o arquivo.</li></ul>

<pre>
  <code>
File.WriteAllText(caminhoArquivoJson, jsonAtualizado);

Console.WriteLine("Dados adicionados com sucesso ao arquivo JSON!");
  </code>
</pre>

