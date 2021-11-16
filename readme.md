```
$ chezmoi add ~/.bashrc
$ chezmoi edit ~/.bashrc

$ chezmoi diff
$ chezmoi -v apply
$ chezmoi merge $FILE
$ chezmoi update -v

$ chezmoi add --autotemplate ~/.gitconfig
$ chezmoi chattr +template ~/.zshrc
```
```
{{- /*  WSL-specific code */}}
{{- if (eq .chezmoi.os "linux") }}
{{-   if (.chezmoi.kernel.osrelease | lower | contains "microsoft") }}
  Actual code goes here
{{-   end }}
{{- end }}

{{- /* MacOS-specific code */}} 
{{- if (eq .chezmoi.os "darwin") }}
  Actual code goes here
{{- end }}
```
