# router
realizando uma exclusão de acordo com a id. Obs.: no postman nao utilizar 
//os dois pontos antes da id 
app.delete('/artigos/remover/:id', (req,res) => {
    let id = req.params.id
    if (id > 0 && id <= artigos.length){
        artigos.splice(id - 1, 1)
        res.status(200).send("Artigo Removido!")
    }else {
        res.status(404).send("Artigo nao encontrado")
    }
})
