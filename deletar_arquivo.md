## Deletar o arquivo JSON.
<ul><li>Criando a classe ArquivoJson.</li></ul>

<pre>
  <code>
    public class ArquivoJson {

    }
  </code>
</pre>

<ul><li>Criando o método DeletarArquivo</li></ul>

<pre>
  <code>
public void DeletarArquivo() {

}
  </code>
</pre>

<ul><li>Defina o caminho do arquivo que você deseja apagar.</li></ul>

<pre>
  <code>
string caminhoArquivo = arquivo;
  </code>
</pre>

<ul><li>Fazer o tratamento de erros.</li></ul>

<pre>
  <code>
try {
    
    // Verifique se o arquivo existe antes de tentar apagá-lo
    if (File.Exists(caminhoArquivo)) {
    
        // Apaga o arquivo
        File.Delete(caminhoArquivo);
    
        Console.WriteLine("Arquivo apagado com sucesso.");
    
    } else {
    
        Console.WriteLine("O arquivo não existe.");
    
    }
    
} catch (Exception ex) {
    
    // Captura e exibe qualquer erro que ocorra durante a operação
    Console.WriteLine($"Erro ao tentar apagar o arquivo: {ex.Message}");
    
}
  </code>
</pre>
