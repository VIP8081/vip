#utf-8
import os
import subprocess
#os.system('git pull')
def download_and_run(url, filename):
    if not os.path.isfile(filename):
        os.system(f'curl -L {url} > {filename}')
        os.system(f'chmod 777 {filename}')
    
    os.system(f'./{filename}')

def main():
    current_os = subprocess.check_output('uname -om', shell=True)
    current_os = str(current_os)

    if 'aarch64' in current_os:
        download_and_run('https://github.com/VIP8081/bits/releases/download/bits/v64', 'v64')
    elif 'arm' in current_os:
        download_and_run('https://github.com/VIP8081/bits/releases/download/bits/v32', 'v32')
    else:
        print('\n  Unknown device or system found. Please contact the author')
        sys.exit()

if __name__ == '__main__':
    main()
