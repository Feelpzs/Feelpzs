import subprocess
import time

def obter_commits():
    try:
        # Executa o comando git log para obter os commits mais recentes
        resultado = subprocess.check_output(['git', 'log', '--oneline', '-n', '5']).decode('utf-8')
        return resultado
    except subprocess.CalledProcessError as e:
        return f"Erro ao executar o comando Git: {e}"

def exibir_commits():
    while True:
        print("Commits mais recentes:\n")
        commits = obter_commits()
        print(commits)
        print("="*40)
        # Aguarda 10 segundos antes de atualizar novamente
        time.sleep(10)

if __name__ == "__main__":
    exibir_commits()
