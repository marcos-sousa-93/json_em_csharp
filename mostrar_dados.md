## Mostrar os dados no console do aplicativo
<ul><li>Criando a classe ArquivoJson.</li></ul>

<pre>
  <code>
public class ArquivoJson {

}
  </code>
</pre>

<ul><li>Criando o método MostrarDados.</li></ul>

<pre>
  <code>
public void MostrarDados() {

}
  </code>
</pre>

<ul><li>Defina o caminho do arquivo JSON.</li></ul>

<pre>
  <code>
string caminhoArquivoJson = arquivo;
  </code>
</pre>

<ul><li>Verifique se o arquivo existe.</li></ul>

<pre>
  <code>
if (File.Exists(caminhoArquivoJson)) {
    // Ler o conteúdo do arquivo JSON
    string jsonExistente = File.ReadAllText(caminhoArquivoJson);
    
    // Desserializar o JSON para uma lista de objetos Pessoa
    List<Pessoa> listaPessoas = JsonConvert.DeserializeObject&#60List&#60Pessoa&#62&#62(jsonExistente);

    // Verificar se há pessoas na lista
    if (listaPessoas != null && listaPessoas.Count &#62 0) {
        // Exibir cada pessoa no console
        foreach (Pessoa pessoa in listaPessoas) {
            Console.WriteLine("Nome: " + pessoa.Nome);
            Console.WriteLine("Idade: " + pessoa.Idade);
            Console.WriteLine("Rua: " + pessoa.Endereco.Rua);
            Console.WriteLine("Cidade: " + pessoa.Endereco.Cidade);
            Console.WriteLine(); // Linha em branco para separar as pessoas
        }
    } else {
        Console.WriteLine("O arquivo JSON está vazio ou não contém dados.");
    }
} else {
    Console.WriteLine("O arquivo JSON não foi encontrado.");
}
  </code>
</pre>
